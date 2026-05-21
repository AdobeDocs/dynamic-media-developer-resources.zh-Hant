---
description: 僅供內部使用。 使用者應該參考影像伺服影像目錄參考 — 屬性參考區段。
solution: Experience Manager
title: getimageservingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ab7b5df6-58fb-4111-be9c-76901534d167
TQID: 'https://experienceleague.adobe.com/-VBxIs4EWFDesksSnU-DpN2pg-LJUN60OPhqjQVqAr8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 80
ht-degree: 16%

---

# getimageservingPublishSettings{#getimageservingpublishsettings}

僅供內部使用。 使用者應該參考影像伺服影像目錄參考 — 屬性參考區段。

語法

## 授權的使用者型別 {#section-49b7b277ba1748499121a0e90996458c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-79f0d54acd604ad2a5c96679334f2424}

**輸入(getImageServingPublishSettingsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 具有影像伺服發佈設定的公司的控制代碼。 |
| contextHandle | `xsd:string` | 是 | 發佈內容的控點。 |

**輸出**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| publishSettingArray | `xsd:string` | 是 | 影像伺服器發佈設定的陣列。 |
