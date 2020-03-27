---
description: 啟用上次修改的回應標題。 啟用或停用影像伺服所發出的可快取HTTP回應中包含「上次修改」標題。
seo-description: 啟用上次修改的回應標題。 啟用或停用影像伺服所發出的可快取HTTP回應中包含「上次修改」標題。
seo-title: UseLastModified
solution: Experience Manager
title: UseLastModified
topic: Scene7 Image Serving - Image Rendering API
uuid: 9dae4f15-4323-4f68-917f-6d72ae52c753
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# UseLastModified{#uselastmodified}

啟用上次修改的回應標題。 啟用或停用影像伺服所發出的可快取HTTP回應中包含「上次修改」標題。

伺服器會使用回應中 `catalog::TimeStamp` 所有目錄／目錄記錄的最新值做為「上次修改」標題值。

只有當使用不支援etag標題的分佈式快取網路或其他快取系統時，才應啟用。

>[!NOTE]
>
>在涉及多台映像服務主機的負載平衡環境中使用上次修改的標頭時，必須小心。 如果由於某些原因，伺服器對同一目錄條目具有不同的時間戳記，則可能會打敗客戶端快取並增加伺服器負載。 這種情況可能發生如下：
>
>* 也 `catalog::TimeStamp` 不 `attribute::TimeStamp`是，因此檔案的修改時 [!DNL catalog.ini] 間將用作預設值 `catalog::TimeStamp`。
   >
   >
* 每台伺服器在本地檔案系統上都有自己的目錄檔案實例，而不是通過網路裝載共用映像目錄檔案。
>* 同一檔案的兩個或多個實例具 [!DNL catalog.ini] 有不同的檔案修改日期，這可能是由於不正確複製檔案所致。
>



## 屬性 {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

標幟. 若要停用，請使用1啟用「上次修改的HTTP」標題。

## 預設 {#section-4eb47aadab8b41609bef296a4115f9f4}

繼承自 `default::UseLastModified` （如果未定義或為空）。

## 另請參閱 {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[目錄：:TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
