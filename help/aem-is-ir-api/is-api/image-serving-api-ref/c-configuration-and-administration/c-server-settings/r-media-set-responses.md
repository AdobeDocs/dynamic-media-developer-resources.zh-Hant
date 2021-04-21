---
description: 本節中的設定適用於由req=set修飾元取得的媒體集回應。
solution: Experience Manager
title: 媒體集響應
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---


# 媒體集響應{#media-set-responses}

本節中的設定適用於由req=set修飾元取得的媒體集回應。

## PS::fvctx.useCatalogRecordValidation —— 快取原則{#section-9accb087d16548a988993bb30395a6f6}

當確定是否需要重新生成從快取中檢索的響應時，此屬性控制快取策略。 如果禁用屬性，則使用[!DNL catalog.ini]檔案的時間戳進行驗證。 如果啟用屬性，則會使用所有參考記錄的最新`catalog::LastModified`時間戳記進行驗證。

## PS::fvctx.nestingLimit —— 巢狀限制{#section-280210341f1647fea02590e7069934d2}

任何`req=set`回應的最大巢狀深度。 如果超出此深度，則會傳回錯誤。

## PS::fvctx.brochureLimit —— 手冊限制{#section-fe36e47db49244cea7f07e9dd3639440}

`req=set`回應中包含所有相關中繼資料的電子目錄手冊數量上限。 一旦超過此限制，任何與手冊項目相關的私人地圖和使用者資料都會被抑制。
