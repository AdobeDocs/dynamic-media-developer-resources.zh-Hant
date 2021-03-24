---
description: IS伺服器可配置為對涉及源映像的請求進行故障切換，這些請求不能成功開啟或讀取。
solution: Experience Manager
title: 錯誤時重新導向
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員、商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 0%

---


# 重新導向錯誤{#redirect-on-error}

IS伺服器可配置為對涉及源映像的請求進行故障切換，這些請求不能成功開啟或讀取。

會重新導向下列類型的請求：

* IS映像，它位於目錄中，但不在磁碟中。

   如果影像未在目錄中，當找不到影像時，不應發生錯誤重新導向。

* 損毀影像、色彩描述檔或字型。
* 在磁碟上找不到靜態內容。

   即使引用的靜態內容沒有目錄記錄，在磁碟上找不到靜態內容請求時，仍會重定向。

在任何其他情況下都不會發生錯誤重新導向。

啟用後，當請求處理期間發生此類錯誤時，主伺服器會將請求傳送至次伺服器進行處理。 然後，無論回應是否表示成功或失敗，都會直接轉送至用戶端。 主伺服器使用快取標籤此類轉發請求的日誌條目。 `REMOTE`主伺服器不在本地快取響應資料。

將`PS::errorRedirect.rootUrl`設為次要伺服器的HTTP網域名稱和埠號，以啟用錯誤重新導向。 此外，連接超時配置為`PS::errorRedirect.connectTimeout` ，並且主伺服器在將錯誤返回到客戶端之前等待從屬伺服器響應的最大時間配置為`PS::errorRedirect.socketTimeout`。

>[!NOTE]
>
>如果無法連接從屬伺服器，則即使配置了預設映像或錯誤映像，也會向客戶端返回文本錯誤響應。

>[!NOTE]
>
>不支援網路路徑中的垂直號字元(|)進行錯誤重新導向。

## 另請參閱 {#section-2e8bfc128b944baf8108279d16492f3f}

[錯誤重定向](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-error-redirection.md#reference-268b1bf6ce1b44bb979727c6f5daf1ac)
