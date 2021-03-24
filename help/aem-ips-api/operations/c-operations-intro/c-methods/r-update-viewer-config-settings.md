---
description: 更新SWF檢視器組態設定。
solution: Experience Manager
title: updateViewerConfigSettings
feature: Dynamic Media經典，SDK/API，檢視器預設集
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 13%

---


# updateViewerConfigSettings{#updateviewerconfigsettings}

更新SWF檢視器組態設定。

語法

## 授權用戶類型{#section-0dd001da1b784aefa5eb5b50c7a2c045}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-29790d933fb24aa392d0cb2d52d1310f}

**輸入(updateViewerConfigSettingsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 為公司負責。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 資產控制代碼。 |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | 是 | 您要套用至檢視器的組態設定陣列。 |

**輸出(updateViewerConfigSettingsReturn)**

IPS API不會傳回此作業的回應。
