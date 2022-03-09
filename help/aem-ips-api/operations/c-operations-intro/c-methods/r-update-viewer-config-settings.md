---
description: 更新SWF查看器配置設定。
solution: Experience Manager
title: updateViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: 04565e2b-bda3-4ad0-afc1-2df01e455490
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 15%

---

# updateViewerConfigSettings{#updateviewerconfigsettings}

更新SWF查看器配置設定。

語法

## 授權用戶類型 {#section-0dd001da1b784aefa5eb5b50c7a2c045}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-29790d933fb24aa392d0cb2d52d1310f}

**輸入(updateViewerConfigSettingsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 把手交給公司。 |
| 資產句柄 | `xsd:string` | 是 | 資產句柄。 |
| configSettingArray | `types:ConfigSettingArray` | 是 | 要應用到查看器的配置設定的陣列。 |

**輸出(updateViewerConfigSettingsReturn)**

IPS API不會為此操作返迴響應。
