---
description: 暈映轉換器(vntc)是命令列公用程式，用來準備使用影像製作功能建立的內容，以便透過影像演算進行部署。
solution: Experience Manager
title: 暈映轉換器
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 0%

---


# 暈映轉換器{#vignette-converter}

暈映轉換器(vntc)是命令列公用程式，用來準備使用影像製作功能建立的內容，以便透過影像演算進行部署。

[!DNL vntc] 位於[!DNL  *[!DNL install_root]*\ImageServing\bin]中。它具備下列功能：

* 將主要暈映轉換為單一解析度、多解析度或金字塔製作暈映（請參閱[暈映縮放](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585)）。
* 生產生產機櫃和窗口，覆蓋樣式檔案（請參見`-resolution`和`-jpegquality`）。

* 可產生不同檔案版本的暈映、檔案櫃和視窗覆蓋樣式檔案，以便與舊版的影像演算搭配使用。
* 從暈映（完整解析度或縮圖）中擷取檢視影像（請參閱`-thumbwidth`和`-image`）。
* 從源檔案中提取相關屬性（請參見`-info`），並將其發送到`stdout`或可選日誌檔案（請參閱`-log`）。

雖然使用[!DNL vntc]是可選的，但強烈建議使用以獲得最佳的伺服器效能。 [!DNL vntc] 此外，還可建置廣泛的錯誤檢查，並可防止在使用時出現嚴重的伺服器問題，包括當機。

產生生產暈映時，輸出暈映的像素寬度（若是金字塔或多解析度暈映，則為0）會附加至產生的輸出暈映檔案名稱。 在處理檔案櫃樣式檔案時，輸出解析度將附加到輸出檔案名。 所有輸出檔案（包括可選縮圖、影像和日誌檔案以及生產暈映或檔案櫃樣式檔案）都放置在&#x200B;*[!DNL sourceFile]*&#x200B;所在的同一目錄中（除非指定了`-destPath`）。

[!DNL vntc] 預設限制為最多3GB的記憶體。當Vntc達到此限制時，它會停止處理並產生錯誤。 此限制可使用`-maxmem`進行變更。

>[!NOTE]
>
>「影像製作」中的暈映更新工具也可用來準備暈映以供影像演算使用。 同樣地，「內容製作工具」也能產生檔案櫃樣式檔案，以便與「影像演算」搭配使用。 如果要自動處理，請使用[!DNL vntc]。 「影像製作」中的工具包含圖形使用者介面，因此通常更容易以互動方式使用。

## 另請參閱 {#section-3c756bf17b634543904fdd928adeafb2}

影像製作檔案
