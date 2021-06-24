---
description: 將檢視器組態設定附加至資產。 這些可以是檢視器預設集或檢視器的來源資產。
solution: Experience Manager
title: setViewerConfigSettings
feature: Dynamic Media Classic, SDK/API，檢視器預設集
role: Developer,Administrator
exl-id: 6b70f2c3-c98b-455f-b453-bb797744dadc
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 10%

---

# setViewerConfigSettings{#setviewerconfigsettings}

將檢視器組態設定附加至資產。 這些可以是檢視器預設集或檢視器的來源資產。

語法

## 授權的使用者類型 {#section-81c429ba9f4c4359986a30ea7ebea8d2}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-bcc8c83cc84141e8b1341be9133e8511}

**輸入(setViewerConfigSettingsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 為公司處理。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 資產控制代碼。 |
| `*`名稱`*` | `xsd:string` | 是 | 資產名稱。 |
| `*`類型`*` | `xsd:string` | 是 | 您要將檢視器設定套用至的資產類型。 |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | 是 | 套用至資產的`ConfigSettings`陣列。 |

**輸出(setViewerConfigSettingsParam)**

IPS API不會針對此操作傳回回應。
