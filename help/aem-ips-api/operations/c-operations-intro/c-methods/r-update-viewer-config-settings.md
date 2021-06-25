---
description: 更新SWF查看器配置設定。
solution: Experience Manager
title: updateViewerConfigSettings
feature: Dynamic Media Classic, SDK/API，檢視器預設集
role: Developer,Administrator
exl-id: 04565e2b-bda3-4ad0-afc1-2df01e455490
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 13%

---

# updateViewerConfigSettings{#updateviewerconfigsettings}

更新SWF查看器配置設定。

語法

## 授權的使用者類型 {#section-0dd001da1b784aefa5eb5b50c7a2c045}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-29790d933fb24aa392d0cb2d52d1310f}

**輸入(updateViewerConfigSettingsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 為公司處理。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 資產控制代碼。 |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | 是 | 您要套用至檢視器的組態設定陣列。 |

**輸出(updateViewerConfigSettingsReturn)**

IPS API不會針對此操作傳回回應。
