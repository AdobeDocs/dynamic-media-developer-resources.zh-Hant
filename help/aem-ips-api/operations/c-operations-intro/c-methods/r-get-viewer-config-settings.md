---
description: 取得與指定資產關聯的所有檢視器組態設定。
solution: Experience Manager
title: getViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: c0438238-8aab-4478-926a-fc0e11732fc1
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 22%

---

# getViewerConfigSettings{#getviewerconfigsettings}

取得與指定資產關聯的所有檢視器組態設定。

語法

## 授權的使用者型別 {#section-05c3ea8f7d2d42c6bf7af63e03f457a9}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-7d06abf3d707494c8a1270c7fa1477f1}

**輸入(getViewerConfigSettingsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 公司處理。 |
| assetHandle | `xsd:string` | 是 | 處理資產。 |

**輸出(getViewerCoinfigSettingsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| type | `xsd:string` | 是 | 組態設定套用的檢視器型別。 |
| configSettingsArray | `types:ConfigSettingsArray` | 是 | 檢視器組態設定的陣列。 |
