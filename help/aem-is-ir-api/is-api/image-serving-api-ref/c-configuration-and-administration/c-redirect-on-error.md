---
description: IS伺服器可配置為對涉及源映像的請求進行故障轉移，這些請求無法成功開啟或讀取。
solution: Experience Manager
title: 錯誤時重定向
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c5541bf3-3296-4ce3-a2ff-9f6336f78ea9
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 0%

---

# 錯誤時重定向{#redirect-on-error}

IS伺服器可配置為對涉及源映像的請求進行故障轉移，這些請求無法成功開啟或讀取。

將重定向以下類型的請求：

* IS映像位於目錄中，但不在磁碟上。

   如果影像不在目錄中，則在找不到影像時不應發生錯誤重定向。

* 損壞的影像、顏色配置檔案或字型。
* 在磁碟上找不到靜態內容。

   在磁碟上找不到靜態內容請求時，即使引用的靜態內容沒有目錄記錄，也會重定向靜態內容請求。

在任何其他情況下都不會發生錯誤重定向。

當啟用時，當在處理請求期間發生此類錯誤時，主伺服器將將請求發送到輔助伺服器以進行處理。 然後將響應直接轉發給客戶機，而不管該響應是指成功還是失敗。 主伺服器標籤此類已轉發請求的日誌條目，並使用快取 `REMOTE`。 主伺服器不在本地快取響應資料。

通過設定啟用錯誤重定向 `PS::errorRedirect.rootUrl` 到輔助伺服器的HTTP域名和埠號。 此外，連接超時配置為 `PS::errorRedirect.connectTimeout` 以及主伺服器在將錯誤返回給配置了的客戶端之前等待從伺服器響應的最長時間 `PS::errorRedirect.socketTimeout`。

>[!NOTE]
>
>如果無法與從屬伺服器聯繫，則即使配置了預設映像或錯誤映像，也會向客戶端返回文本錯誤響應。

>[!NOTE]
>
>網路路徑中的管道字元(|)不支援錯誤重定向。

## 另請參閱 {#section-2e8bfc128b944baf8108279d16492f3f}

[重定向錯誤](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-error-redirection.md#reference-268b1bf6ce1b44bb979727c6f5daf1ac)
