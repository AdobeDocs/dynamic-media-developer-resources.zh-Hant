---
description: IS伺服器可配置為對涉及源映像的請求進行故障切換，這些請求不能成功開啟或讀取。
seo-description: IS伺服器可配置為對涉及源映像的請求進行故障切換，這些請求不能成功開啟或讀取。
seo-title: 錯誤時重新導向
solution: Experience Manager
title: 錯誤時重新導向
topic: Scene7 Image Serving - Image Rendering API
uuid: 894babe9-9c3c-4972-ae8f-387d65b4167d
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 0%

---


# 錯誤時重新導向{#redirect-on-error}

IS伺服器可配置為對涉及源映像的請求進行故障切換，這些請求不能成功開啟或讀取。

會重新導向下列類型的請求：

* IS映像，它位於目錄中，但不在磁碟中。

   如果影像未在目錄中，當找不到影像時，不應發生錯誤重新導向。

* 損毀影像、色彩描述檔或字型。
* 在磁碟上找不到靜態內容。

   即使引用的靜態內容沒有目錄記錄，在磁碟上找不到靜態內容請求時，仍會重定向。

在任何其他情況下都不會發生錯誤重新導向。

啟用後，當請求處理期間發生此類錯誤時，主伺服器會將請求傳送至次伺服器進行處理。 然後，無論回應是否表示成功或失敗，都會直接轉送至用戶端。 主伺服器用快取來標籤此類轉發請求的日誌條目 `REMOTE`。 主伺服器不在本地快取響應資料。

錯誤重新導向是通過 `PS::errorRedirect.rootUrl` 設定為從屬伺服器的HTTP域名和埠號來啟用的。 此外，連接超時配置為 `PS::errorRedirect.connectTimeout` ，並且主伺服器在將錯誤返回客戶端之前等待輔助伺服器響應的最長時間配置為 `PS::errorRedirect.socketTimeout`。

>[!NOTE]
>
>如果無法連絡從屬伺服器，則會傳回文字錯誤回應給用戶端，即使已設定預設影像或錯誤影像亦然。

>[!NOTE]
>
>不支援網路路徑中的垂直號字元(|)進行錯誤重新導向。

## 另請參閱 {#section-2e8bfc128b944baf8108279d16492f3f}

[錯誤重定向](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-error-redirection.md#reference-268b1bf6ce1b44bb979727c6f5daf1ac)
