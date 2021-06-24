---
description: 僅供內部使用。 使用者應參考「影像伺服影像目錄參考 — 屬性參考」區段。
solution: Experience Manager
title: getImageServingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: ab7b5df6-58fb-4111-be9c-76901534d167
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 15%

---

# getImageServingPublishSettings{#getimageservingpublishsettings}

僅供內部使用。 使用者應參考「影像伺服影像目錄參考 — 屬性參考」區段。

語法

## 授權的使用者類型 {#section-49b7b277ba1748499121a0e90996458c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-79f0d54acd604ad2a5c96679334f2424}

**輸入(getImageServingPublishSettingsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 具有影像提供發佈設定之公司的控制代碼。 |
| `*`contextHandle`*` | `xsd:string` | 是 | 處理發佈內容。 |

**輸出**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`publishSettingArray`*` | `xsd:string` | 是 | 影像伺服器發佈設定的陣列。 |
