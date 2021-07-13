---
description: 一般伺服器設定
solution: Experience Manager
title: 一般
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: 3e4079e7-6def-4938-bb5b-c8122502712d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 1%

---

# 一般{#general}

一般伺服器設定

## TC::PsPort — 主偵聽埠 {#section-d31d3051aa994a76b60b70c3d9f7e89f}

指定Platform Server的主偵聽埠。 此連接埠也用於存取影像提供、影像轉譯和Dynamic Media檢視器（如果已安裝）的檔案和範例頁面。

## IS::CacheServerUrl — 快取服務根Url {#section-bcca227a1f91453b834db4ea050968e2}

指定HTTP根路徑，以允許影像伺服器訪問快取服務。 必須設定為[!DNL http://localhost:TC::PsPort /is/cache/secondary]，埠號與`TC::PsPort`匹配。

## IS::RemoteUrlDefaultExpiration — 遠端Image Source預設TTL {#section-e4c31228b459492cacd2f482d9575f71}

使用`src={…}`結構從遠端來源透過HTTP取得的快取影像TTL。 僅當遠程伺服器的HTTP響應中未包含Expiration標題時使用。 以秒為單位的整數值。

## IS::RemoteUrlTimeout — 遠端Image Source逾時 {#section-437646c479cc4bea81dae42100a3c50a}

影像伺服器等待遠程伺服器通過HTTP傳送請求的影像檔案，然後返回錯誤的時間。 以秒為單位的整數值。

## PS::allowDefaultCatalogRequests — 啟用/停用預設目錄請求 {#section-484e442a115a49b4ac269d1718b351e1}

設為false以禁止在路徑中包含有效目錄ID的請求。 預設為 `true`. 設為`false`時，系統會針對沒有目錄ID的請求傳回錯誤。

>[!NOTE]
>
>`req=catalogprops` 不受此設定的限制。

## PS::saveToFile.saveTimeout — 檔案保存超時 {#section-d22afd8ad86144b28684ed95a59db40e}

未指定`timeout=`時`req=saveToFile`的預設超時值。 `msec`. 如果儲存操作未在指定的時間內完成，則會傳回錯誤。
