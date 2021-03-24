---
description: 「影像轉換」支援根據符合ICC（國際色彩協會）規格的色域描述檔進行色域轉換。
solution: Experience Manager
title: 影像演算色彩管理*
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 0%

---


# 影像演算色彩管理*{#image-rendering-color-management}

「影像轉換」支援根據符合ICC（國際色彩協會）規格的色域描述檔進行色域轉換。

**限制**

目前僅支援CMYK、RGB和灰階色彩空間。

檔案櫃樣式檔案(.vnc)和窗口覆蓋樣式檔案([!DNL .vnw])不受顏色管理，並且假定存在於工作色域中。

**另請參閱**

[International Color Consortium](http://www.color.org/index.xalter) ,  [ `icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06) ,  [ `iccEmbed=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f) ,  `attribute::IccProfile*` ,  `attribute::IccProfileSrc*`,  `attribute::IccRenderIntent`  `attribute::IccBlackPointCompensation`  `attribute::IccDither` ICC Profile Maps

## 預設色域{#section-8ce27edf42e746febe4654f8f19b9c0c}

每個影像目錄（和預設目錄）都可以定義一組ICC描述檔。 這些描述檔構成此目錄的預設色域——灰階、RGB和CMYK資料（`attribute::IccProfileRgb`、`attribute::IccProfileGray`、`attribute::IccProfileCmyk`、`attribute::IccProfileSrcRgb`、`attribute::IccProfileSrcGray`和`attribute::IccProfileSrcCmyk`）各一個輸入和一個輸出描述檔。

特定影像或其它對象的預設顏色空間是根據影像的像素類型從目錄預設配置檔案中選擇的。

## 輸入色域{#section-660f661a7e954df4b451e34134195276}

材料影像可嵌入ICC描述檔以定義輸入顏色空間。 如果源影像中沒有嵌入配置檔案，則將使用與源影像的像素類型對應的適用影像目錄的`attribute::IccProfileSrc*`。 如果未在映像目錄中定義此屬性，則使用`attribute::IccProfile*`。 如果未定義該目錄屬性，則影像不受色彩管理，只套用天真的變形。

## 工作色域{#section-645d9cfa5b0347a190a0ece218f5b5e1}

通常，工作色域由內嵌在暈映中的ICC色彩描述檔定義。 如果暈映不包含描述檔，則會將預設的RGB輸入描述檔（作業目錄的`attribute::IccProfileSrcRgb`）用於工作色域。

所有渲染操作都在工作色域中執行。

**重要：** 使用中色域的ICC描述檔必須支援輸入和輸出轉換。如果僅輸出配置檔案用作工作色域，IR將無法將材料轉換為工作色域。 如果材料存在於相同的工作色域中，則仍然可以使用這種顏色輪廓。 嘗試在其他色域中套用材質將會失敗。

## 顯式顏色值{#section-31727bf1b23e477ca92572fbbf422d2f}

使用`color=`、`bgc=`、`catalog::BgColor`和`catalog::Color`指定的RGB顏色值假定存在於當前工作顏色空間中。

## 材料資料檔案{#section-33f7a170a6664c02b8479fb89cc0aea3}

材質影像檔案（紋理和貼花影像）可以有RGB、灰階或CMYK像素類型，而且可以內嵌色彩描述檔。 如果未嵌入顏色配置檔案，則預設輸入顏色空間與影像相關聯（例如，來自材料目錄的顏色配置檔案，該顏色配置檔案與影像的像素類型相對應）。

從巢狀「影像伺服」或「影像轉換」請求取得的材質影像通常包含色彩描述檔。 如果不是，影像會與像素類型對應的預設輸入色域產生關聯。

如果影像檔案的顏色空間與工作顏色空間不同，則使用精確的顏色轉換來轉換為工作顏色空間。 當未嵌入配置檔案且未定義預設輸入配置檔案時，將使用天真類型轉換。

其他材料資料檔案(如檔案櫃樣式檔案([!DNL .vnc])或窗口覆蓋檔案([!DNL .vnw]))不嵌入顏色配置檔案，並始終假定在工作色域中。

## 輸出色域{#section-4c2c4dfedbb8429ba5cfddc3d3eab6c4}

所有渲染操作都在工作色域中進行。 如果請求使用`icc=`命令指定不同的色彩描述檔，資料會在編碼並傳回至用戶端之前，先轉換為該色彩空間。 當停用色彩管理時，若需要將轉換為灰階或CMYK，則會使用天真的轉換。

## 內嵌的色彩描述檔{#section-5ff733832d38429fbe02b3c1e9bb94a9}

通過為請求指定`iccEmbed=`，可以將與渲染影像相關聯的顏色配置檔案嵌入到響應影像中。

如果未指定`icc=`，則嵌入工作色域的ICC配置檔案。 如果禁用色彩管理且未使用`icc=`指定任何描述檔，則不會嵌入任何描述檔。

## ICC 設定檔 {#section-afeb76068b5042adb83261638e450140}

伺服器使用的所有顏色配置檔案都必須符合ICC規範。 ICC配置檔案通常具有[!DNL .icc]或[!DNL .icm]檔案尾碼，並與材料資料檔案共同定位。

雖然輸出配置檔案可以由`icc=`命令中的檔案路徑／名稱指定，但建議在預設目錄或特定材料目錄的ICC配置檔案映射中註冊所有配置檔案，並使用快捷方式標識符(`icc::Name`)而不是檔案路徑。

工作配置檔案必須在物料目錄或預設目錄的ICC配置檔案映射中註冊。
