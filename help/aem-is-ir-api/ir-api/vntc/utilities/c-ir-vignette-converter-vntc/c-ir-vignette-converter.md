---
description: 暈映轉換器(vntc)是命令列公用程式，用來準備使用影像製作功能建立的內容，以便透過影像演算進行部署。
seo-description: 暈映轉換器(vntc)是命令列公用程式，用來準備使用影像製作功能建立的內容，以便透過影像演算進行部署。
seo-title: 暈映轉換器
solution: Experience Manager
title: 暈映轉換器
topic: Scene7 Image Serving - Image Rendering API
uuid: b32a30d6-ae4a-406f-88a9-e8b0eec394c9
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---


# 暈映轉換器{#vignette-converter}

暈映轉換器(vntc)是命令列公用程式，用來準備使用影像製作功能建立的內容，以便透過影像演算進行部署。

[!DNL vntc] 位於[!DNL *[!DNL install_root]*\ImageServing\bin]中。 它具備下列功能：

* 將主要暈映轉換為單一解析度、多解析度或金字塔製作暈映(請參 [閱暈映縮放](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585))。
* 製作包含樣式檔的生產機櫃和視窗(請參 `-resolution` 閱和 `-jpegquality`)。

* 可產生不同檔案版本的暈映、檔案櫃和視窗覆蓋樣式檔案，以便與舊版的影像演算搭配使用。
* 從暈映（完整解析度或縮圖）中擷取檢視影像(請參 `-thumbwidth` 閱和 `-image`)。
* 從來源檔案擷取相關屬性(請參 `-info`閱)，並將其傳送至 `stdout` 或選用的記錄檔(請參閱 `-log`)。

雖然使用是可選 [!DNL vntc] 的，但強烈建議使用它以獲得最佳的伺服器效能。 [!DNL vntc] 此外，還可建置廣泛的錯誤檢查，並可防止在使用時出現嚴重的伺服器問題，包括當機。

產生生產暈映時，輸出暈映的像素寬度（若是金字塔或多解析度暈映，則為0）會附加至產生的輸出暈映檔案名稱。 在處理檔案櫃樣式檔案時，輸出解析度將附加到輸出檔案名。 所有輸出檔案（包括可選縮圖、影像和記錄檔）以及生產暈映或檔案櫃樣式檔案都放置在所 *[!DNL sourceFile]* 在的同 `-destPath` 一目錄中（除非指定）。

[!DNL vntc] 預設限制為最多3GB的記憶體。 當Vntc達到此限制時，它會停止處理並產生錯誤。 此限制可使用變更 `-maxmem`。

>[!NOTE]
>
>「影像製作」中的暈映更新工具也可用來準備暈映以供影像演算使用。 同樣地，「內容製作工具」也能產生檔案櫃樣式檔案，以便與「影像演算」搭配使用。 如果 [!DNL vntc] 要自動處理，請使用。 「影像製作」中的工具包含圖形使用者介面，因此通常更容易以互動方式使用。

## 另請參閱 {#section-3c756bf17b634543904fdd928adeafb2}

影像製作檔案
