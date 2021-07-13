---
description: 對伺服器快取使用這些伺服器設定。
solution: Experience Manager
title: 伺服器快取
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: 6a8d44d3-ecac-4fe0-9f81-28b1cd55e7e1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# 伺服器快取{#server-caches}

對伺服器快取使用這些伺服器設定。

## PS::cache.rootPaths — 快取資料夾 {#section-f0aa808304d74ecdb0c3644f11906c53}

平台伺服器的磁碟快取的根資料夾。 相對於&#x200B;*[!DNL install_folder]*&#x200B;的一個或多個絕對檔案路徑或路徑，用分號(;)分隔。 HTTP回應快取的資料將平均分配給所有指定的資料夾。 輔助快取的快取（編譯的影像目錄和外部影像資料）將位於主快取資料夾（清單中的第一個資料夾）中。

## PS::cache.maxSize — 響應資料快取大小 {#section-ed2e1e7ba4bd4e13b77bb20c4cacddb4}

HTTP響應快取的最大大小（以位元組為單位）。 此設定會限制要快取的實際資料量；它不考慮檔案系統開銷。 （請參閱[回應資料快取](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-data-caches/c-response-data-cache.md#concept-81ea996c242441f2a69f7e9d9b3a29ca)。） 如果指定了多個快取資料夾，快取資料將平均分佈在所有資料夾中。 [!DNL PlatformServer.conf]中的`cache.maxSize`值是位元組。

## PS::cache.maxEntries — 回應資料快取最大項 {#section-5603e327e90542a5b50aeeb27b080410}

為記憶體內HTTP響應快取索引分配的項數。

>[!NOTE]
>
>在Linux上，確保為快取分區分配了足夠的i節點，以避免i節點耗盡。

## IS::TempDirectory — 映像伺服器臨時檔案資料夾 {#section-42ea1e7a68c444878f7245c5bbcb1672}

映像伺服器偶爾需要將中間資料保存到磁碟。 路徑可以是絕對路徑，也可以是相對於&#x200B;*[!DNL install_folder]*&#x200B;的路徑。

>[!NOTE]
>
>更改此設定之前必須建立新資料夾。 請確定已設定存取權限，讓影像伺服器完全控制資料夾。

## SV::temp — 伺服器主管臨時檔案資料夾 {#section-fd2cd5ef7e814a4bb56aaf5525e1a154}

伺服器主管偶爾需要將中間資料保存到磁碟。 路徑可以是絕對路徑，也可以是相對於&#x200B;*[!DNL install_folder]*&#x200B;的路徑。 預設為[!DNL *[!DNL install_folder]*/temp]。

>[!NOTE]
>
>更改此設定之前必須建立新資料夾。 確保已設定訪問權限，以便伺服器主管能夠完全控制資料夾。
