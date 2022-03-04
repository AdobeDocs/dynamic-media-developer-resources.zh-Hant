---
description: 「影像渲染」支援基於符合ICC（國際色彩聯盟）規範的色彩空間配置檔案的色彩空間轉換。
solution: Experience Manager
title: 影像呈現顏色管理*
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa772ab2-8a32-4c1a-9ee3-c1cf4a0b3095
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '736'
ht-degree: 0%

---

# 影像呈現顏色管理*{#image-rendering-color-management}

「影像渲染」支援基於符合ICC（國際色彩聯盟）規範的色彩空間配置檔案的色彩空間轉換。

**限制**

目前僅支援CMYK、RGB和灰階色彩空間。

檔案櫃樣式檔案(.vnc)和窗口覆蓋樣式檔案( [!DNL .vnw])未進行顏色管理，並假定工作顏色空間中存在。

**另請參閱**

[國際顏色聯盟](https://www.color.org/index.xalter) 。 [ `icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06) 。 [ `iccEmbed=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f) 。 `attribute::IccProfile*` 。 `attribute::IccProfileSrc*`。 `attribute::IccRenderIntent` 。 `attribute::IccBlackPointCompensation` 。 `attribute::IccDither` , ICC配置檔案映射

## 預設顏色空格 {#section-8ce27edf42e746febe4654f8f19b9c0c}

每個影像目錄（和預設目錄）都可以定義一組ICC配置檔案。 這些配置檔案構成了此目錄的預設顏色空間 — 灰階、RGB和CMYK資料的一個輸入和一個輸出配置檔案( `attribute::IccProfileRgb`。 `attribute::IccProfileGray`。 `attribute::IccProfileCmyk`。 `attribute::IccProfileSrcRgb`。 `attribute::IccProfileSrcGray`, `attribute::IccProfileSrcCmyk`)。

根據影像的像素類型從目錄預設配置檔案中選擇特定影像或其他對象的預設顏色空間。

## 輸入顏色空間 {#section-660f661a7e954df4b451e34134195276}

材料影像可以嵌入ICC配置檔案以定義輸入顏色空間。 如果源影像中沒有嵌入配置檔案， `attribute::IccProfileSrc*` 使用對應於源影像的像素類型的適用影像目錄。 如果未在影像目錄中定義此屬性， `attribute::IccProfile*` 的子菜單。 如果也未定義該目錄屬性，則影像不受顏色管理，只應用天真的轉換。

## 工作色彩空間 {#section-645d9cfa5b0347a190a0ece218f5b5e1}

通常，工作顏色空間由嵌入在視圖中的ICC顏色配置檔案定義。 如果視圖不包括配置檔案，則預設RGB輸入配置檔案( `attribute::IccProfileSrcRgb` 會話目錄)用於工作顏色空間。

在工作顏色空間中執行所有渲染操作。

**重要提示：** 工作顏色空間的ICC配置檔案必須支援輸入和輸出轉換。 如果僅輸出配置檔案用作工作色彩空間，則IR將無法將材料轉換為它。 如果材料存在於相同的工作顏色空間中，則仍可使用這種顏色輪廓。 嘗試在其他顏色空間中應用材料將失敗。

## 顯式顏色值 {#section-31727bf1b23e477ca92572fbbf422d2f}

RGB顏色值 `color=`。 `bgc=`。 `catalog::BgColor`, `catalog::Color` 假設存在於當前工作顏色空間中。

## 材料資料檔案 {#section-33f7a170a6664c02b8479fb89cc0aea3}

材料影像檔案（紋理和貼花影像）可具有RGB、灰度或CMYK像素類型，並可嵌入顏色配置檔案。 如果未嵌入顏色配置檔案，則預設輸入顏色空間與影像相關聯（例如，與影像的像素類型對應的材料目錄中的顏色配置檔案）。

從嵌套的「影像服務」或「影像渲染」請求獲得的材料影像通常包括顏色配置檔案。 如果不是，則影像與與像素類型對應的預設輸入顏色空間相關聯。

如果影像檔案的顏色空間不同於工作顏色空間，則使用精確的顏色轉換來轉換為工作顏色空間。 未嵌入配置檔案且未定義預設輸入配置檔案時，將使用天真類型轉換。

其他材料資料檔案，如檔案櫃樣式檔案( [!DNL .vnc])或覆蓋檔案的窗口( [!DNL .vnw])不嵌入顏色配置檔案，並且始終假定它位於工作顏色空間中。

## 輸出顏色空間 {#section-4c2c4dfedbb8429ba5cfddc3d3eab6c4}

所有渲染操作都在工作顏色空間中進行。 如果請求使用 `icc=` 命令，資料將在編碼前轉換為該顏色空間並返回給客戶端。 禁用顏色管理時，如果需要轉換為灰階或CMYK，則使用天真的轉換。

## 嵌入式顏色配置檔案 {#section-5ff733832d38429fbe02b3c1e9bb94a9}

通過指定與所呈現的影像相關聯的顏色輪廓可以嵌入到響應影像中 `iccEmbed=` 請求。

如果 `icc=` 未指定，則嵌入工作顏色空間的ICC配置檔案。 如果禁用顏色管理且未指定配置式，則不嵌入配置式 `icc=`。

## ICC 設定檔 {#section-afeb76068b5042adb83261638e450140}

伺服器使用的所有顏色配置檔案必須符合ICC規範。 ICC配置檔案通常具有 [!DNL .icc] 或 [!DNL .icm] 檔案尾碼，與材料資料檔案共址。

而輸出配置檔案可以通過 `icc=` 命令，建議在預設目錄或特定材料目錄的「ICC配置檔案映射」中註冊所有配置檔案，並使用快捷方式標識符( `icc::Name`)而不是檔案路徑。

必須在物料目錄或預設目錄的「ICC配置檔案映射」中註冊工作配置檔案。
