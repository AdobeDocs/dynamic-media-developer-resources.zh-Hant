---
title: 暈映轉換工具
description: 暈映轉換程式(vntc)是一個命令列公用程式，用來準備使用「影像製作」建立的內容，以便使用「影像演算」進行部署。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9e2ad2d4-9061-41d1-941b-8be4c17a6c43
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---

# 暈映轉換工具{#vignette-converter}

暈映轉換程式(vntc)是一個命令列公用程式，用來準備使用「影像製作」建立的內容，以便使用「影像演算」進行部署。

[!DNL vntc]位於[!DNL *[!DNL install_root]*\ImageServing\bin]。 它有以下功能：

* 將主要暈映轉換為單解析度、多解析度或金字塔製作暈映（請參閱[暈映縮放](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585)）。
* 產生生產封包和涵蓋樣式檔案的視窗（請參閱`-resolution`和`-jpegquality`）。

* 產生不同版本的暈映、檔案櫃和視窗覆蓋物樣式檔案，以搭配較舊版本的「影像演算」使用。
* 從完整解析度或縮圖的暈映擷取檢視影像（請參閱`-thumbwidth`和`-image`）。
* 從來源檔案擷取相關屬性（請參閱`-info`），並將它們傳送至`stdout`或選用的記錄檔（請參閱`-log`）。

雖然[!DNL vntc]的使用是選擇性的，但Adobe建議使用它以獲得最佳伺服器效能。 暈映轉換工具也會執行廣泛的錯誤檢查，並可防止嚴重伺服器問題，包括當機問題（若勤奮使用時）。

產生生產暈映時，輸出暈映的畫素寬度（如果金字塔或多解析度暈映，則為0）會附加至產生的輸出暈映檔案的名稱。 處理封包樣式檔案時，輸出解析度會附加至輸出檔案名稱。 所有輸出檔案，包括選用的縮圖、影像和記錄檔以及生產暈映或封包樣式檔案，都置於&#x200B;*[!DNL sourceFile]*&#x200B;所在的相同目錄中（除非指定`-destPath`）。

根據預設，暈映轉換器的記憶體限製為最多3 GB。 當vntc達到此限制時，它會停止處理並產生錯誤。 可使用`-maxmem`變更此限制。

>[!NOTE]
>
>影像製作中的暈映更新工具也可用來準備暈映以供影像演算使用。 同樣地，「內容製作工具」可以產生檔案櫃樣式檔案，以與「影像演算」搭配使用。 若要自動處理，請使用[!DNL vntc]。 「影像製作」中的工具包含圖形化使用者介面，因此通常更易於以互動方式使用。

## 另請參閱 {#section-3c756bf17b634543904fdd928adeafb2}

影像製作檔案
