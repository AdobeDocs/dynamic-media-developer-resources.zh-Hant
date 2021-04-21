---
description: 將檢視器組態設定附加至資產。 這些預設可以是檢視器預設集或檢視器的來源資產。
solution: Experience Manager
title: setViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 10%

---


# setViewerConfigSettings{#setviewerconfigsettings}

將檢視器組態設定附加至資產。 這些預設可以是檢視器預設集或檢視器的來源資產。

語法

## 授權用戶類型{#section-81c429ba9f4c4359986a30ea7ebea8d2}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-bcc8c83cc84141e8b1341be9133e8511}

**輸入(setViewerConfigSettingsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 為公司負責。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 資產控制代碼。 |
| `*`名稱`*` | `xsd:string` | 是 | 資產名稱。 |
| `*`類型`*` | `xsd:string` | 是 | 您要套用檢視器設定的資產類型。 |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | 是 | `ConfigSettings`的陣列應用於資產。 |

**輸出(setViewerConfigSettingsParam)**

IPS API不會傳回此作業的回應。
