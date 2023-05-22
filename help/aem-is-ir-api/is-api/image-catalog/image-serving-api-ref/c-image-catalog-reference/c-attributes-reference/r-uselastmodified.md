---
description: 啟用上次修改的響應標頭。 啟用或禁用映像服務發出的可快取HTTP響應中包含上次修改的標頭。
solution: Experience Manager
title: 使用上次修改時間
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4908da5d-636e-44d2-bd49-40e01c8b5f79
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 1%

---

# 使用上次修改時間{#uselastmodified}

啟用上次修改的響應標頭。 啟用或禁用映像服務發出的可快取HTTP響應中包含上次修改的標頭。

伺服器使用最新 `catalog::TimeStamp` 響應中涉及的所有目錄/目錄記錄的值作為上次修改的標題值。

僅當使用不支援etag標頭的分佈式快取網路或其他快取系統時才應啟用。

>[!NOTE]
>
>在涉及多個映像服務主機的負載平衡環境中使用上次修改的報頭時，必須小心。 如果由於某種原因，伺服器對同一目錄項具有不同的時間戳，則客戶端快取可能會失敗，伺服器負載會增加。 這種情況可能發生如下：
>
>* 都不 `catalog::TimeStamp` 無 `attribute::TimeStamp`，因此修改時間 [!DNL catalog.ini] 檔案用作 `catalog::TimeStamp`。
>
>* 每個伺服器不是通過網路裝載共用映像目錄檔案，而是在本地檔案系統上具有其自己的目錄檔案實例。
>* 兩個或多個相同實例 [!DNL catalog.ini] 檔案的檔案修改日期不同，可能是由於檔案複製不當所致。
>


## 屬性 {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

標幟. 0禁用，1啟用上次修改的HTTP標頭。

## 預設 {#section-4eb47aadab8b41609bef296a4115f9f4}

繼承自 `default::UseLastModified` 或為空。

## 另請參閱 {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[目錄：:TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
