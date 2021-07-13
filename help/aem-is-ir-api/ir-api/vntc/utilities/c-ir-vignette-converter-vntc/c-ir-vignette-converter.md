---
description: 暈映轉換器(vntc)是一個命令行實用程式，用於準備使用影像創作建立的內容，以便通過影像渲染進行部署。
solution: Experience Manager
title: 暈映轉換器
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9e2ad2d4-9061-41d1-941b-8be4c17a6c43
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---

# 暈映轉換器{#vignette-converter}

暈映轉換器(vntc)是一個命令行實用程式，用於準備使用影像創作建立的內容，以便通過影像渲染進行部署。

[!DNL vntc] 位於[!DNL  *[!DNL install_root]*\ImageServing\bin]。其功能如下：

* 將主要暈映轉換為單解析度、多解析度或金字塔產生暈映（請參閱[暈映縮放](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585)）。
* 生成包含樣式檔案的生產機櫃和窗口（請參見`-resolution`和`-jpegquality`）。

* 可以生成不同檔案版本的暈映、檔案櫃和窗口覆蓋樣式檔案，以便與舊版的影像渲染一起使用。
* 從暈映中擷取檢視影像，可以是完整解析度或縮圖（請參閱`-thumbwidth`和`-image`）。
* 從源檔案中提取相關屬性（請參閱`-info`）並將其發送到`stdout`或可選日誌檔案（請參閱`-log`）。

雖然使用[!DNL vntc]是可選的，但強烈建議使用它以獲得最佳伺服器效能。 [!DNL vntc] 此外，還會實作廣泛的錯誤檢查，並可防止認真使用時出現嚴重的伺服器問題，包括當機。

產生生產暈映時，輸出暈映的像素寬度（若是金字塔或多解析度暈映，則為0）會附加至所產生輸出暈映檔案的名稱。 處理檔案櫃樣式檔案時，輸出解析度會附加至輸出檔案名稱。 所有輸出檔案（包括可選縮略圖、影像和日誌檔案以及生產暈映或機櫃樣式檔案）都放置在&#x200B;*[!DNL sourceFile]*&#x200B;所在的同一目錄中（除非指定`-destPath`）。

[!DNL vntc] 預設限制為最多3GB記憶體。當Vntc達到此限制時，會停止處理並產生錯誤。 此限制可使用`-maxmem`進行更改。

>[!NOTE]
>
>影像製作中的暈映更新工具也可用來準備暈映以供影像轉譯使用。 同樣地，「內容創作工具」能夠生成用於影像渲染的檔案櫃樣式檔案。 如果要自動處理，請使用[!DNL vntc]。 影像製作中的工具包含圖形使用者介面，因此通常可更輕鬆互動地使用。

## 另請參閱 {#section-3c756bf17b634543904fdd928adeafb2}

影像製作檔案
