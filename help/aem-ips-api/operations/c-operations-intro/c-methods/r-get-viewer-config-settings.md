---
description: 取得與指定資產相關聯的所有檢視器組態設定。
solution: Experience Manager
title: getViewerConfigSettings
feature: Dynamic Media Classic, SDK/API，檢視器預設集
role: Developer,Administrator
exl-id: c0438238-8aab-4478-926a-fc0e11732fc1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 20%

---

# getViewerConfigSettings{#getviewerconfigsettings}

取得與指定資產相關聯的所有檢視器組態設定。

語法

## 授權的使用者類型 {#section-05c3ea8f7d2d42c6bf7af63e03f457a9}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-7d06abf3d707494c8a1270c7fa1477f1}

**輸入(getViewerConfigSettingsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 為公司處理。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 處理資產。 |

**輸出(getViewerCoinfigSettingsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`類型`*` | `xsd:string` | 是 | 配置設定要套用的查看器類型。 |
| `*`configSettingsArray`*` | `types:ConfigSettingsArray` | 是 | 檢視器組態設定陣列。 |
