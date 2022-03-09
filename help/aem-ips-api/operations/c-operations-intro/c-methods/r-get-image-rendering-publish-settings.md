---
description: 僅供內部使用。 請參閱「影像渲染材料目錄參考 — 目錄屬性」部分。
solution: Experience Manager
title: getImageRenderingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 152dfd61-2fba-47b4-8e69-fbbc8fb57f87
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 17%

---

# getImageRenderingPublishSettings{#getimagerenderingpublishsettings}

僅供內部使用。 請參閱「影像渲染材料目錄參考 — 目錄屬性」部分。

語法

## 授權用戶類型 {#section-1097e0563c61480a8e97822dc3527070}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-4f2cb8c589384816bb2525654ec49963}

**輸入(getImageRenderingPublishSettingsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 要獲取其影像呈現發佈設定的公司的句柄。 |
| 上下文句柄 | `xsd:string` | 是 | 處理發佈上下文。 |

**輸出(getImageRenderingPublishSettingsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| publishSettingsArray | `type:ConfigSettingArray` | 是 | 影像呈現發佈設定。 |
