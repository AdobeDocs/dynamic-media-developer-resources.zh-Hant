---
description: 常規伺服器設定
solution: Experience Manager
title: 一般
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3e4079e7-6def-4938-bb5b-c8122502712d
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 1%

---

# 一般{#general}

常規伺服器設定

## TC::PsPort — 主偵聽埠 {#section-d31d3051aa994a76b60b70c3d9f7e89f}

指定主監聽埠 [!DNL Platform Server]。 此埠還用於訪問影像服務、影像呈現和Dynamic Media查看器（如果已安裝）的文檔和示例頁。

## IS::CacheServerUrl — 快取服務根URL {#section-bcca227a1f91453b834db4ea050968e2}

指定HTTP根路徑，以允許Image Server訪問快取服務。 必須設定為 [!DNL http://localhost:TC::PsPort /is/cache/secondary]，埠號匹配 `TC::PsPort`。

## IS::RemoteUrlDefaultExpiration — 遠程Image Source預設TTL {#section-e4c31228b459492cacd2f482d9575f71}

通過HTTP從遠程源使用 `src={…}` 構造。 僅在遠程伺服器的HTTP響應中不包含到期報頭時使用。 整數值（以秒為單位）。

## IS::RemoteUrlTimeout — 遠程Image Source超時 {#section-437646c479cc4bea81dae42100a3c50a}

映像伺服器在返回錯誤之前等待遠程伺服器通過HTTP傳遞請求的映像檔案的時間。 整數值（以秒為單位）。

## PS::allowDefaultCatalogRequests — 啟用/禁用預設目錄請求 {#section-484e442a115a49b4ac269d1718b351e1}

設定為false禁止在路徑中不包含有效目錄ID的請求。 預設為 `true`. 設定為時 `false`，對於沒有目錄ID的請求返回錯誤。

>[!NOTE]
>
>`req=catalogprops` 不受此設定的限制。

## PS::saveToFile.saveTimeout — 檔案保存超時 {#section-d22afd8ad86144b28684ed95a59db40e}

預設超時值 `req=saveToFile` 何時 `timeout=`未指定。 `msec`. 如果保存操作未在指定的時間內完成，則返回錯誤。
