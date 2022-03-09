---
description: 僅供內部使用。 用戶應參考「Image Serving Image Catalog Reference - Attribute Reference」部分。
solution: Experience Manager
title: getImageServingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ab7b5df6-58fb-4111-be9c-76901534d167
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 16%

---

# getImageServingPublishSettings{#getimageservingpublishsettings}

僅供內部使用。 用戶應參考「Image Serving Image Catalog Reference - Attribute Reference」部分。

語法

## 授權用戶類型 {#section-49b7b277ba1748499121a0e90996458c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-79f0d54acd604ad2a5c96679334f2424}

**輸入(getImageServingPublishSettingsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 具有提供發佈設定的影像的公司的句柄。 |
| 上下文句柄 | `xsd:string` | 是 | 處理發佈上下文。 |

**輸出**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| publishSettingArray | `xsd:string` | 是 | 映像伺服器發佈設定的陣列。 |
