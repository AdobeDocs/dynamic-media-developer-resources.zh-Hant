---
description: 本節中的設定適用於由req=set修飾符獲得的媒體集響應。
solution: Experience Manager
title: 媒體集回應
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: e3833726-d345-4741-8096-d74f299ac9fc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---

# 媒體集回應{#media-set-responses}

本節中的設定適用於由req=set修飾符獲得的媒體集響應。

## PS::fvctx.useCatalogRecordValidation — 快取策略 {#section-9accb087d16548a988993bb30395a6f6}

當確定是否需要重新生成從快取中檢索到的響應時，此屬性控制快取策略。 如果禁用屬性，則使用[!DNL catalog.ini]檔案的時間戳進行驗證。 如果啟用屬性，則會使用所有參考記錄的最新`catalog::LastModified`時間戳記進行驗證。

## PS::fvctx.nestingLimit — 嵌套限制 {#section-280210341f1647fea02590e7069934d2}

任何`req=set`響應的最大嵌套深度。 如果超過此深度，則會傳回錯誤。

## PS::fvctx.brochureLimit — 手冊限制 {#section-fe36e47db49244cea7f07e9dd3639440}

`req=set`響應中包含所有關聯元資料的電子目錄手冊的最大數量。 一旦超過此限制，與手冊項目相關的任何私人地圖和用戶資料都會被隱藏。
