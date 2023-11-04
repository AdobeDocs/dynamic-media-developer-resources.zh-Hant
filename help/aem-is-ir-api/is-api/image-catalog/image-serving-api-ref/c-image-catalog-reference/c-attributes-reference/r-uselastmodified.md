---
description: 啟用上次修改的回應標頭。 啟用或停用在影像伺服發出的可快取HTTP回應中包含Last-Modified標頭。
solution: Experience Manager
title: UseLastModified
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4908da5d-636e-44d2-bd49-40e01c8b5f79
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 1%

---

# UseLastModified{#uselastmodified}

啟用上次修改的回應標頭。 啟用或停用在影像伺服發出的可快取HTTP回應中包含Last-Modified標頭。

伺服器使用最近的 `catalog::TimeStamp` 回應中涉及的所有目錄/目錄記錄的值，做為Last-Modified標頭值。

只有在使用的分散式快取網路或其他快取系統不支援etag標題時，才應啟用。

>[!NOTE]
>
>在涉及多個影像伺服主機的負載平衡環境中使用Last-Modified標題時，應謹慎處理。 如果由於某些原因，伺服器對於相同的目錄專案具有不同的時間戳記，使用者端快取可能會失敗且伺服器負載會增加。 這種情況可能會發生：
>
>* 兩者皆非 `catalog::TimeStamp` 也不 `attribute::TimeStamp`，因此修改時間 [!DNL catalog.ini] 檔案為的預設值 `catalog::TimeStamp`.
>
>* 每個伺服器在本機檔案系統上都有自己的目錄檔案執行個體，而不是透過網路掛載來共用影像目錄檔案。
>* 兩個或多個相同的例項 [!DNL catalog.ini] 檔案有不同的檔案修改日期，可能是因為檔案複製不當所造成。
>

## 屬性 {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

標幟. 0代表停用，1代表啟用Last-Modified HTTP標題。

## 預設 {#section-4eb47aadab8b41609bef296a4115f9f4}

繼承自 `default::UseLastModified` 若未定義或為空。

## 另請參閱 {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[catalog：：TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
