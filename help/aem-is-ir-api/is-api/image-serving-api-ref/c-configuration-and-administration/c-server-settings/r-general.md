---
description: 一般伺服器設定
solution: Experience Manager
title: 一般
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 1%

---


# 一般{#general}

一般伺服器設定

## TC::PsPort —— 主監聽埠{#section-d31d3051aa994a76b60b70c3d9f7e89f}

指定平台伺服器的主監聽埠。 此埠也用於存取影像伺服、影像演算和Dynamic Media檢視器（如果已安裝）的檔案和範例頁面。

## IS::CacheServerUrl - Caching Service根Url {#section-bcca227a1f91453b834db4ea050968e2}

指定HTTP根路徑，以允許影像伺服器訪問快取服務。 必須設定為[!DNL http://localhost:TC::PsPort /is/cache/secondary] ，埠號與`TC::PsPort`匹配。

## IS::RemoteUrlDefaultExpiration —— 遠程映像源預設TTL {#section-e4c31228b459492cacd2f482d9575f71}

使用`src={…}`結構從遠程源通過HTTP獲取的快取影像的TTL。 僅在遠程伺服器的HTTP響應中不包含「過期」標題時使用。 整數值（以秒為單位）。

## IS::RemoteUrlTimeout —— 遠程映像源超時{#section-437646c479cc4bea81dae42100a3c50a}

映像伺服器等待遠程伺服器通過HTTP傳送請求的映像檔案，然後返回錯誤的時間。 整數值（以秒為單位）。

## PS::allowDefaultCatalogRequests —— 啟用／停用預設目錄請求{#section-484e442a115a49b4ac269d1718b351e1}

設為false可禁止路徑中未包含有效目錄ID的請求。 預設為 `true`. 設為`false`時，若請求沒有目錄ID，則會傳回錯誤。

>[!NOTE]
>
>`req=catalogprops` 不受此設定的約束。

## PS::saveToFile.saveTimeout —— 檔案保存超時{#section-d22afd8ad86144b28684ed95a59db40e}

未指定`timeout=`時`req=saveToFile`的預設逾時值。 `msec`. 如果在指定的時間內未完成保存操作，將返回錯誤。
