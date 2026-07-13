---
description: 更新SWF檢視器組態設定。
solution: Experience Manager
title: updateViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: 04565e2b-bda3-4ad0-afc1-2df01e455490
TQID: 'https://experienceleague.adobe.com/YcfK5U6MKvmV2ulOQ3s2sOOBsgASSeslCIrk87xLAv8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 59
ht-degree: 15%

---

# updateViewerConfigSettings{#updateviewerconfigsettings}

更新SWF檢視器組態設定。

語法

## 授權的使用者型別 {#section-0dd001da1b784aefa5eb5b50c7a2c045}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-29790d933fb24aa392d0cb2d52d1310f}

**輸入(updateViewerConfigSettingsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 公司處理。 |
| assetHandle | `xsd:string` | 是 | 資產控制代碼。 |
| configSettingArray | `types:ConfigSettingArray` | 是 | 您要套用至檢視器的組態設定陣列。 |

**輸出(updateViewerConfigSettingsReturn)**

IPS API未傳回此作業的回應。

