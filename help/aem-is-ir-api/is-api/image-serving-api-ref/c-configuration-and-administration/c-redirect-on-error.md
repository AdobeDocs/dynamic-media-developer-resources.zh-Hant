---
description: IS伺服器可設定成容錯移轉至其他伺服器，以處理無法成功開啟或讀取來源影像的要求。
solution: Experience Manager
title: 發生錯誤時重新導向
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c5541bf3-3296-4ce3-a2ff-9f6336f78ea9
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# 發生錯誤時重新導向{#redirect-on-error}

IS伺服器可設定成容錯移轉至其他伺服器，以處理無法成功開啟或讀取來源影像的要求。

系統會重新導向下列型別的請求：

* IS影像在目錄中但不在磁碟上。

  如果影像不在目錄中，則在找不到影像時，不應發生錯誤重新導向。

* 損壞的影像、色彩設定檔或字型。
* 在磁碟上找不到靜態內容。

  在磁碟上找不到靜態內容請求時，即使參考的靜態內容沒有目錄記錄，也會重新導向。

在其他任何情況下都不會發生錯誤重新導向。

當啟用以及在處理請求期間發生這類錯誤時，主要伺服器會將請求傳送至次要伺服器以進行處理。 然後會將回應（無論是否表示成功或失敗）直接轉送給使用者端。 主要伺服器使用快取來標籤此類轉送要求的記錄專案`REMOTE`。 主要伺服器不會在本機快取回應資料。

將`PS::errorRedirect.rootUrl`設定為次要伺服器的HTTP網域名稱和連線埠號碼，即可啟用錯誤重新導向。 此外，連線逾時設定為`PS::errorRedirect.connectTimeout`，而主要伺服器等待次要伺服器回應的最長時間，則在傳回錯誤給使用者端之前設定為`PS::errorRedirect.socketTimeout`。

>[!NOTE]
>
>如果無法連絡次要伺服器，則會傳回文字錯誤回應給使用者端，即使已設定預設影像或錯誤影像亦然。

>[!NOTE]
>
>網路路徑中的管路字元(|)不支援錯誤重新導向。

## 另請參閱 {#section-2e8bfc128b944baf8108279d16492f3f}

[錯誤重新導向](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-error-redirection.md#reference-268b1bf6ce1b44bb979727c6f5daf1ac)
