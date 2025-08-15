---
description: 使用這些伺服器設定進行伺服器快取。
solution: Experience Manager
title: 伺服器快取
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 6a8d44d3-ecac-4fe0-9f81-28b1cd55e7e1
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# 伺服器快取{#server-caches}

使用這些伺服器設定進行伺服器快取。

## PS：：cache.rootPaths — 快取資料夾 {#section-f0aa808304d74ecdb0c3644f11906c53}

[!DNL Platform Server]的磁碟快取的根資料夾。 相對於&#x200B;*[!DNL install_folder]*&#x200B;的一或多個絕對檔案路徑或路徑，以分號(；)分隔。 HTTP回應快取的資料會平均分配到所有指定的資料夾。 輔助快取的快取（編譯的影像目錄和外部影像資料）位於主要快取資料夾（清單中的第一個資料夾）中。

## PS：：cache.maxSize — 回應資料快取大小 {#section-ed2e1e7ba4bd4e13b77bb20c4cacddb4}

HTTP回應快取的大小上限（位元組）。 此設定會限制要快取的實際資料量，不會考慮檔案系統額外負荷。 （請參閱[回應資料快取](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-data-caches/c-response-data-cache.md#concept-81ea996c242441f2a69f7e9d9b3a29ca)。）如果指定了多個快取資料夾，則快取資料會平均分佈在所有資料夾中。 `cache.maxSize`中[!DNL PlatformServer.conf]的值是位元組。

## PS：：cache.maxEntries — 回應資料快取專案上限 {#section-5603e327e90542a5b50aeeb27b080410}

配置給記憶體內HTTP回應快取索引的專案數。

>[!NOTE]
>
>在Linux上，請確定為快取分割配置足夠的i-node，以避免i-node用盡。

## IS：：TempDirectory — 影像伺服器暫存檔案資料夾 {#section-42ea1e7a68c444878f7245c5bbcb1672}

影像伺服器偶爾需要將中繼資料儲存到磁碟。 路徑可以是絕對或相對於&#x200B;*[!DNL install_folder]*。

>[!NOTE]
>
>必須先建立新資料夾，才能變更此設定。 請確定存取許可權已設定，讓影像伺服器可完全控制資料夾。

## SV：：temp — 伺服器監督員暫存檔案資料夾 {#section-fd2cd5ef7e814a4bb56aaf5525e1a154}

伺服器管理員偶爾需要將中繼資料儲存到磁碟。 路徑可以是絕對或相對於&#x200B;*[!DNL install_folder]*。 預設為[！DNL *[!DNL install_folder]*/temp]。

>[!NOTE]
>
>必須先建立新資料夾，才能變更此設定。 請確定已設定存取許可權，讓伺服器管理員可以完全控制資料夾。
