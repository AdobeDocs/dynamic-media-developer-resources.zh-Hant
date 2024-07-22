---
description: 「影像演算」支援根據符合ICC （國際色彩聯盟）規格的色域設定檔進行色域轉換。
solution: Experience Manager
title: 影像演算色彩管理*
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa772ab2-8a32-4c1a-9ee3-c1cf4a0b3095
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '731'
ht-degree: 0%

---

# 影像演算色彩管理*{#image-rendering-color-management}

「影像演算」支援根據符合ICC （國際色彩聯盟）規格的色域設定檔進行色域轉換。

**限制**

目前僅支援CMYK、RGB和灰階色域。

封包樣式檔案(.vnc)和視窗覆蓋樣式檔案([!DNL .vnw])不是色彩管理檔案，而且假設它們存在於工作色域中。

**另請參閱**

[國際色彩協會](https://www.color.org/index.xalter) ， [`icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06) ， [`iccEmbed=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f) ， `attribute::IccProfile*` ， `attribute::IccProfileSrc*`， `attribute::IccRenderIntent` ， `attribute::IccBlackPointCompensation` ， `attribute::IccDither` ， ICC設定檔地圖

## 預設色彩空間 {#section-8ce27edf42e746febe4654f8f19b9c0c}

每個影像目錄（和預設目錄）可以定義一組ICC設定檔。 這些設定檔構成此目錄的預設色彩空間 — 灰階、RGB和CMYK資料（ `attribute::IccProfileRgb`、`attribute::IccProfileGray`、`attribute::IccProfileCmyk`、`attribute::IccProfileSrcRgb`、`attribute::IccProfileSrcGray`和`attribute::IccProfileSrcCmyk`）各有一個輸入和一個輸出設定檔。

系統會根據影像的畫素型別，從目錄預設設定檔中選取特定影像或其他物件的預設色域。

## 輸入色域 {#section-660f661a7e954df4b451e34134195276}

材質影像可內嵌ICC設定檔以定義輸入色域。 如果來源影像中沒有內嵌設定檔，則會使用與來源影像的畫素型別對應的適用影像目錄`attribute::IccProfileSrc*`。 如果未在影像目錄中定義此屬性，則會使用`attribute::IccProfile*`。 如果未定義該目錄屬性，則影像不會以色彩管理，只會套用天真的轉換。

## 工作色域 {#section-645d9cfa5b0347a190a0ece218f5b5e1}

通常，作用色域是由內嵌在暈映中的ICC色彩設定檔所定義。 如果暈映不包含設定檔，則會將預設RGB輸入設定檔（工作階段目錄的`attribute::IccProfileSrcRgb`）用於工作色域。

所有演算作業都會在工作色域中執行。

**重要：**&#x200B;使用中色域的ICC設定檔必須支援輸入和輸出轉換。 如果僅輸出設定檔用作工作色域，IR無法將材質轉換為它。 如果材質存在於相同的工作色域中，仍可使用這種色彩輪廓。 嘗試在其他色域中套用材質失敗。

## 明確的顏色值 {#section-31727bf1b23e477ca92572fbbf422d2f}

以`color=`、`bgc=`、`catalog::BgColor`和`catalog::Color`指定的RGB色彩值假設存在於目前的工作色域中。

## 材質資料檔案 {#section-33f7a170a6664c02b8479fb89cc0aea3}

材質影像檔案（紋理和貼花影像）可以有RGB、灰階或CMYK畫素型別，也可以內嵌色彩設定檔。 如果未內嵌色彩設定檔，預設的輸入色域會與影像相關聯（例如，與影像畫素型別相對應的材質目錄中的色彩設定檔）。

從巢狀影像提供或影像演算請求獲得的材質影像通常包含色彩設定檔。 如果不是這種情況，影像會與畫素型別對應的預設輸入色域相關聯。

如果影像檔案的色域與作用中的色域不同，則會使用精確的色彩轉換來轉換為作用中的色域。 若未內嵌設定檔且未定義預設輸入設定檔，則會使用樸素型別轉換。

其他材質資料檔案，例如封包樣式檔案([!DNL .vnc])或視窗涵蓋範圍檔案([!DNL .vnw])不會內嵌色彩設定檔，且一律會假設為位於工作色域中。

## 輸出色域 {#section-4c2c4dfedbb8429ba5cfddc3d3eab6c4}

所有演算作業都會在工作色域中進行。 如果要求使用`icc=`命令指定不同的色彩設定檔，資料會先轉換至該色彩空間，然後才進行編碼並傳回使用者端。 停用色彩管理時，會使用天真的轉換（如有必要）來轉換為灰階或CMYK。

## 內嵌色彩設定檔 {#section-5ff733832d38429fbe02b3c1e9bb94a9}

藉由為要求指定`iccEmbed=`，與演算後的影像相關聯的色彩設定檔可以嵌入回應影像中。

如果未指定`icc=`，則會內嵌工作色域的ICC設定檔。 如果停用色彩管理且沒有使用`icc=`指定設定檔，則不會內嵌設定檔。

## ICC 設定檔 {#section-afeb76068b5042adb83261638e450140}

伺服器使用的所有色彩設定檔都必須符合ICC規格。 ICC設定檔通常有[!DNL .icc]或[!DNL .icm]檔案字尾，並與素材資料檔共用。

雖然輸出設定檔可以由`icc=`命令中的檔案路徑/名稱指定，但建議在預設目錄或特定材質目錄的ICC設定檔對應中註冊所有設定檔，並使用捷徑識別碼( `icc::Name`)而不是檔案路徑。

必須在材料目錄或預設目錄的「ICC設定檔對映」中註冊工作設定檔。
