---
description: 取得與指定資產相關聯的所有檢視器組態設定。
solution: Experience Manager
title: getViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 19%

---


# getViewerConfigSettings{#getviewerconfigsettings}

取得與指定資產相關聯的所有檢視器組態設定。

語法

## 授權用戶類型{#section-05c3ea8f7d2d42c6bf7af63e03f457a9}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-7d06abf3d707494c8a1270c7fa1477f1}

**輸入(getViewerConfigSettingsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 為公司負責。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 處理資產。 |

**輸出(getViewerCoinfigSettingsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`類型`*` | `xsd:string` | 是 | 設定設定套用至的檢視器類型。 |
| `*`configSettingsArray`*` | `types:ConfigSettingsArray` | 是 | 檢視器組態設定的陣列。 |

