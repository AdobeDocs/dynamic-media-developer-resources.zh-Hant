---
description: 取得與指定資產相關聯的所有檢視器組態設定。
seo-description: 取得與指定資產相關聯的所有檢視器組態設定。
seo-title: getViewerConfigSettings
solution: Experience Manager
title: getViewerConfigSettings
topic: Scene7 Image Production System API
uuid: 61fe16de-ac72-472b-8945-f1ebe8b4d11c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getViewerConfigSettings{#getviewerconfigsettings}

取得與指定資產相關聯的所有檢視器組態設定。

語法

## 授權使用者類型 {#section-05c3ea8f7d2d42c6bf7af63e03f457a9}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-7d06abf3d707494c8a1270c7fa1477f1}

**輸入(getViewerConfigSettingsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 是 | 為公司負責。 |
| ` *`assetHandle`*` | `xsd:string` | 是 | 處理資產。 |

**輸出(getViewerCoinfigSettingsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`類型`*` | `xsd:string` | 是 | 設定設定套用至的檢視器類型。 |
| ` *`configSettingsArray`*` | `types:ConfigSettingsArray` | 是 | 檢視器組態設定的陣列。 |

