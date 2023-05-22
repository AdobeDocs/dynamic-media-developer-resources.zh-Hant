---
description: 本節中的設定適用於由req=set修飾符獲取的媒體集響應。
solution: Experience Manager
title: 媒體集響應
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e3833726-d345-4741-8096-d74f299ac9fc
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# 媒體集響應{#media-set-responses}

本節中的設定適用於由req=set修飾符獲取的媒體集響應。

## PS::fvctx.useCatalogRecordValidation — 快取策略 {#section-9accb087d16548a988993bb30395a6f6}

當確定是否需要重新生成從快取檢索到的響應時，此屬性控制快取策略。 如果禁用屬性，則 [!DNL catalog.ini] 檔案用於驗證。 如果啟用了屬性，則 `catalog::LastModified` 所有引用記錄的時間戳用於驗證。

## PS::fvctx.netsingLimit — 嵌套限制 {#section-280210341f1647fea02590e7069934d2}

任何嵌套的最大深度 `req=set` 回應。 如果超出此深度，則返回錯誤。

## PS::fvctx.brochureLimit — 手冊限制 {#section-fe36e47db49244cea7f07e9dd3639440}

電子目錄手冊的最大數量 `req=set` 包含所有關聯元資料的響應。 一旦超過此限制，則禁止與小冊子項目相關聯的任何私有地圖和用戶資料。
