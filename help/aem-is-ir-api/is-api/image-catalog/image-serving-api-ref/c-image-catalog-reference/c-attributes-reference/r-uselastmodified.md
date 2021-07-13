---
description: 啟用上次修改的回應標題。 啟用或停用將上次修改的標題包含在影像伺服發出的可快取HTTP回應中。
solution: Experience Manager
title: UseLastModified
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4908da5d-636e-44d2-bd49-40e01c8b5f79
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 2%

---

# UseLastModified{#uselastmodified}

啟用上次修改的回應標題。 啟用或停用將上次修改的標題包含在影像伺服發出的可快取HTTP回應中。

伺服器將響應中涉及的所有目錄/目錄記錄的最近`catalog::TimeStamp`值用作上次修改的標題值。

只有在使用不支援標頭的分佈式快取網路或其他快取系統時，才應啟用。

>[!NOTE]
>
>在涉及多個影像服務主機的負載平衡環境中使用上次修改的標題時，請務必小心。 如果伺服器對相同目錄項目有不同的時間戳記，則可能會失敗用戶端快取並增加伺服器負載。 這種情況可能發生如下：
>
>* `catalog::TimeStamp`和`attribute::TimeStamp`均不存在，因此[!DNL catalog.ini]檔案的修改時間將用作`catalog::TimeStamp`的預設時間。
   >
   >
* 每台伺服器在本地檔案系統上都有其自己的目錄檔案實例，而不是通過網路裝載共用映像目錄檔案。
>* 同一[!DNL catalog.ini]檔案的兩個或多個實例具有不同的檔案修改日期，這可能是由於檔案的複製不當所致。

>



## 屬性 {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

標幟. 若要停用，請使用1啟用上次修改的HTTP標題。

## 預設 {#section-4eb47aadab8b41609bef296a4115f9f4}

如果未定義或為空，則從`default::UseLastModified`繼承。

## 另請參閱 {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[目錄：:TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
