---
description: 僅供內部使用。 使用者應參考「影像伺服影像目錄參考——屬性參考」區段。
solution: Experience Manager
title: getImageServingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 14%

---


# getImageServingPublishSettings{#getimageservingpublishsettings}

僅供內部使用。 使用者應參考「影像伺服影像目錄參考——屬性參考」區段。

語法

## 授權用戶類型{#section-49b7b277ba1748499121a0e90996458c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-79f0d54acd604ad2a5c96679334f2424}

**輸入(getImageServingPublishSettingsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 具有影像伺服發佈設定的公司控制代碼。 |
| `*`contextHandle`*` | `xsd:string` | 是 | 處理發佈內容。 |

**輸出**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`publishSettingArray`*` | `xsd:string` | 是 | 影像伺服器發佈設定的陣列。 |

