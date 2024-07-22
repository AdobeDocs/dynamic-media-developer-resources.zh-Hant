---
title: 媒體集回應
description: 本節中的設定適用於由req=set修飾元取得的媒體集回應。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e3833726-d345-4741-8096-d74f299ac9fc
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# 媒體集回應{#media-set-responses}

此區段中的設定適用於由`req=set`修飾元取得的媒體集回應。

## PS：：fvctx.useCatalogRecordValidation — 快取原則 {#section-9accb087d16548a988993bb30395a6f6}

此屬性可控制當決定是否必須重新產生從快取中擷取的設定回應時，快取原則。 如果屬性已停用，則會使用[!DNL catalog.ini]檔案的時間戳記進行驗證。 如果啟用屬性，則會使用所有參考記錄中的最新`catalog::LastModified`時間戳記進行驗證。

## PS：：fvctx.nestingLimit — 巢狀限制 {#section-280210341f1647fea02590e7069934d2}

任何`req=set`回應的最大巢狀深度。 如果超過此深度，則會傳回錯誤。

## PS：：fvctx.brochureLimit — 手冊上限 {#section-fe36e47db49244cea7f07e9dd3639440}

包含所有關聯中繼資料的`req=set`回應中，電子目錄手冊的最大數量。 一旦超過此限制，就會隱藏與手冊專案相關的任何私人地圖和使用者資料。
