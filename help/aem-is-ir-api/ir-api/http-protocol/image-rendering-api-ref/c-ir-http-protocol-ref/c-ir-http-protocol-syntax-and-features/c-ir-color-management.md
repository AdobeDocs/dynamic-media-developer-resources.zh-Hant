---
description: 影像呈現支援基於符合ICC（國際顏色協會）規範的顏色空間配置檔案的顏色空間轉換。
solution: Experience Manager
title: 影像轉譯色彩管理*
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: fa772ab2-8a32-4c1a-9ee3-c1cf4a0b3095
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '743'
ht-degree: 0%

---

# 影像轉譯色彩管理*{#image-rendering-color-management}

影像呈現支援基於符合ICC（國際顏色協會）規範的顏色空間配置檔案的顏色空間轉換。

**限制**

目前僅支援CMYK、RGB和灰階色域。

檔案櫃樣式檔案(.vnc)和窗口覆蓋樣式檔案([!DNL .vnw])不受顏色管理，假定存在於工作顏色空間中。

**另請參閱**

[國際色彩協會](http://www.color.org/index.xalter) 、  [ `icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06) 、  [ `iccEmbed=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f) 、  `attribute::IccProfile*` 、  `attribute::IccProfileSrc*`、  `attribute::IccRenderIntent` 、  `attribute::IccBlackPointCompensation` 、  `attribute::IccDither` 、ICC設定檔地圖

## 預設色域 {#section-8ce27edf42e746febe4654f8f19b9c0c}

每個影像目錄（和預設目錄）都可以定義一組ICC配置檔案。 這些配置檔案構成此目錄的預設顏色空間 — 每個配置檔案分別用於灰度級、RGB和CMYK資料（`attribute::IccProfileRgb`、`attribute::IccProfileGray`、`attribute::IccProfileCmyk`、`attribute::IccProfileSrcRgb`、`attribute::IccProfileSrcGray`和`attribute::IccProfileSrcCmyk`）。

根據影像的像素類型，從目錄預設配置檔案中選擇特定影像或其它對象的預設顏色空間。

## 輸入色域 {#section-660f661a7e954df4b451e34134195276}

材料影像可以嵌入ICC輪廓以定義輸入顏色空間。 如果源影像中未嵌入任何輪廓，則將使用與源影像的像素類型對應的適用影像目錄的`attribute::IccProfileSrc*`。 如果未在影像目錄中定義此屬性，則使用`attribute::IccProfile*`。 如果該目錄屬性也未定義，則影像不會受色彩管理，而僅套用天真轉換。

## 工作色域 {#section-645d9cfa5b0347a190a0ece218f5b5e1}

通常，工作色域由內嵌於暈映中的ICC顏色配置檔案定義。 如果暈映不包含配置檔案，則工作色域將使用預設的RGB輸入配置檔案（會話目錄的`attribute::IccProfileSrcRgb`）。

所有渲染操作都在工作顏色空間中執行。

**重要：** 工作色域的ICC配置檔案必須支援輸入和輸出轉換。如果將僅輸出輪廓用作工作色空間，則IR將無法將材料轉換為工作色空間。 如果材料存在於相同的工作顏色空間中，則仍然可以使用這種顏色輪廓。 嘗試在其他顏色空間中應用材料將失敗。

## 顯式顏色值 {#section-31727bf1b23e477ca92572fbbf422d2f}

使用`color=`、`bgc=`、`catalog::BgColor`和`catalog::Color`指定的RGB顏色值假定存在於當前工作顏色空間中。

## 材料資料檔案 {#section-33f7a170a6664c02b8479fb89cc0aea3}

材料影像檔案（紋理和底色影像）可以具有RGB、灰度級或CMYK像素類型，並可以嵌入顏色輪廓。 如果未嵌入任何顏色輪廓，則預設輸入顏色空間與影像相關聯（例如，來自材料目錄的顏色輪廓，該顏色輪廓與影像的像素類型相對應）。

從巢狀影像提供或影像轉譯請求獲得的材料影像通常包含顏色描述檔。 若非如此，則影像會與與像素類型對應的預設輸入顏色空間相關聯。

如果影像檔案的顏色空間與工作顏色空間不同，則使用精確的顏色轉換來轉換為工作顏色空間。 當未嵌入配置檔案且未定義預設輸入配置檔案時，將使用天真類型轉換。

其他材料資料檔案，如檔案櫃樣式檔案([!DNL .vnc])或覆蓋檔案([!DNL .vnw])的窗口檔案，不嵌入顏色配置檔案，並且始終假定位於工作顏色空間中。

## 輸出色域 {#section-4c2c4dfedbb8429ba5cfddc3d3eab6c4}

所有渲染操作都在工作顏色空間中進行。 如果請求使用`icc=`命令指定不同的顏色配置檔案，則資料將在編碼前轉換為該顏色空間並返回給客戶端。 當禁用顏色管理時，如果需要將其轉換為灰度或CMYK，則使用天真轉換。

## 嵌入的顏色配置檔案 {#section-5ff733832d38429fbe02b3c1e9bb94a9}

通過為請求指定`iccEmbed=`，可以將與呈現影像相關聯的顏色配置檔案嵌入到響應影像中。

如果未指定`icc=`，則嵌入工作顏色空間的ICC配置檔案。 如果禁用顏色管理，並且未使用`icc=`指定配置檔案，則不嵌入配置檔案。

## ICC 設定檔 {#section-afeb76068b5042adb83261638e450140}

伺服器使用的所有顏色配置檔案都必須符合ICC規範。 ICC配置檔案通常具有[!DNL .icc]或[!DNL .icm]檔案尾碼，並與材料資料檔案共用。

雖然可以在`icc=`命令中由檔案路徑/名稱指定輸出配置檔案，但建議在預設目錄或特定材料目錄的ICC配置檔案映射中註冊所有配置檔案，並使用快捷方式標識符(`icc::Name`)，而不是檔案路徑。

必須在物料目錄或預設目錄的ICC配置檔案映射中註冊工作配置檔案。
