---
description: Vignette Converter(vntc)是一個命令行實用程式，用於準備使用「影像創作」建立的內容，以便通過「影像渲染」進行部署。
solution: Experience Manager
title: Vignette轉換器
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9e2ad2d4-9061-41d1-941b-8be4c17a6c43
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# Vignette轉換器{#vignette-converter}

Vignette Converter(vntc)是一個命令行實用程式，用於準備使用「影像創作」建立的內容，以便通過「影像渲染」進行部署。

[!DNL vntc] 位於[!DNL中 *[!DNL install_root]*\ImageServing\bin]。 它具有以下功能：

* 將主小圖轉換為單解析度、多解析度或金字塔生產小圖（請參見） [維涅特縮放](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585))。
* 生成包含樣式檔案的生產檔案櫃和窗口(請參閱 `-resolution` 和 `-jpegquality`)。

* 可以生成不同檔案版本的小圖、檔案櫃和窗口覆蓋樣式檔案，以便與較舊版本的「影像渲染」一起使用。
* 從小圖（完全解析度或縮略圖）中提取視圖影像(請參閱 `-thumbwidth` 和 `-image`)。
* 從源檔案中提取相關屬性(請參見 `-info`)並將其發送 `stdout` 或可選日誌檔案(請參見 `-log`)。

使用 [!DNL vntc] 是可選的，強烈建議使用它來獲得最佳伺服器效能。 [!DNL vntc] 此外，還可以執行大量錯誤檢查，並可以防止認真使用時出現嚴重的伺服器問題，包括崩潰。

在生成生產小角符時，輸出小角符（在金字塔或多解析度小角符的情況下為0）的像素寬度被附加到生成的輸出小角符檔案的名稱上。 處理CAB樣式檔案時，輸出解析度將附加到輸出檔案名後。 所有輸出檔案（包括可選的縮略圖、影像和日誌檔案以及生產視圖或檔案櫃樣式檔案）都放在同一目錄下，其中 *[!DNL sourceFile]* 位於(除非 `-destPath` 指定)。

[!DNL vntc] 預設情況下，將自身限制為最多3GB記憶體。 當Vntc達到此限制時，它將停止處理並產生錯誤。 此限制可使用 `-maxmem`。

>[!NOTE]
>
>影像創作中的Vignette更新工具也可用於準備圖片以用於影像渲染。 同樣，內容創作工具能夠生成用於影像渲染的檔案櫃樣式檔案。 使用 [!DNL vntc] 自動處理。 「影像創作」中的工具包括圖形用戶介面，因此通常更容易交互使用。

## 另請參閱 {#section-3c756bf17b634543904fdd928adeafb2}

影像創作文檔
