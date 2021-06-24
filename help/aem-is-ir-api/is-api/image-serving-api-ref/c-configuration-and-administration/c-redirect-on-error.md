---
description: IS伺服器可配置為針對涉及源映像的請求故障切換到備用伺服器，這些源映像無法成功開啟或讀取。
solution: Experience Manager
title: 出現錯誤時重新導向
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: c5541bf3-3296-4ce3-a2ff-9f6336f78ea9
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# 出現錯誤時重新導向{#redirect-on-error}

IS伺服器可配置為針對涉及源映像的請求故障切換到備用伺服器，這些源映像無法成功開啟或讀取。

系統會重新導向下列類型的請求：

* 是目錄中的映像，但不是磁碟上的映像。

   如果影像不在目錄中，當找不到影像時，不應發生錯誤重新導向。

* 損壞的影像、顏色配置檔案或字型。
* 在磁碟上找不到靜態內容。

   在磁碟上找不到靜態內容請求時，即使引用的靜態內容沒有目錄記錄，靜態內容請求也會被重新導向。

在任何其他情況下都不會發生錯誤重新導向。

當啟用時，當請求處理期間發生此類錯誤時，主要伺服器會將請求傳送至次要伺服器進行處理。 無論回應是否指出成功或失敗，都會直接轉送至用戶端。 主伺服器使用`REMOTE`快取來標籤此類轉發請求的日誌條目。 主伺服器不會在本機快取回應資料。

將`PS::errorRedirect.rootUrl`設定為次伺服器的HTTP域名和埠號，以啟用錯誤重定向。 此外，連接超時配置為`PS::errorRedirect.connectTimeout`，主伺服器在將錯誤返回給客戶端之前等待從次伺服器響應的最大時間配置為`PS::errorRedirect.socketTimeout`。

>[!NOTE]
>
>如果無法聯繫次伺服器，則將向客戶端返回文本錯誤響應，即使配置了預設影像或錯誤影像亦然。

>[!NOTE]
>
>錯誤重定向不支援網路路徑中的垂直號字元(|)。

## 另請參閱 {#section-2e8bfc128b944baf8108279d16492f3f}

[錯誤重定向](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-error-redirection.md#reference-268b1bf6ce1b44bb979727c6f5daf1ac)
