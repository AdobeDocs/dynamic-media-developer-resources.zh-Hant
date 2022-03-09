---
description: 將查看器配置設定附加到資產。 這些可以是查看器預設或查看器的源資產。
solution: Experience Manager
title: setViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: 6b70f2c3-c98b-455f-b453-bb797744dadc
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 12%

---

# setViewerConfigSettings{#setviewerconfigsettings}

將查看器配置設定附加到資產。 這些可以是查看器預設或查看器的源資產。

語法

## 授權用戶類型 {#section-81c429ba9f4c4359986a30ea7ebea8d2}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-bcc8c83cc84141e8b1341be9133e8511}

**輸入(setViewerConfigSettingsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 把手交給公司。 |
| 資產句柄 | `xsd:string` | 是 | 資產句柄。 |
| 名稱 | `xsd:string` | 是 | 資產名稱。 |
| type | `xsd:string` | 是 | 要應用查看器配置的資產類型。 |
| configSettingArray | `types:ConfigSettingArray` | 是 | 陣列 `ConfigSettings` 應用於資產…… |

**輸出(setViewerConfigSettingsParam)**

IPS API不會為此操作返迴響應。
