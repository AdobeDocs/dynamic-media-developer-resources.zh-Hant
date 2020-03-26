---
description: 更新SWF檢視器組態設定。
seo-description: 更新SWF檢視器組態設定。
seo-title: updateViewerConfigSettings
solution: Experience Manager
title: updateViewerConfigSettings
topic: Scene7 Image Production System API
uuid: ad4af874-5ca4-4182-868e-afa48b1cd2b6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# updateViewerConfigSettings{#updateviewerconfigsettings}

更新SWF檢視器組態設定。

語法

## 授權使用者類型 {#section-0dd001da1b784aefa5eb5b50c7a2c045}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-29790d933fb24aa392d0cb2d52d1310f}

**輸入(updateViewerConfigSettingsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 是 | 為公司負責。 |
| ` *`assetHandle`*` | `xsd:string` | 是 | 資產控制代碼。 |
| ` *`configSettingArray`*` | `types:ConfigSettingArray` | 是 | 您要套用至檢視器的組態設定陣列。 |

**輸出(updateViewerConfigSettingsReturn)**

IPS API不會傳回此作業的回應。
