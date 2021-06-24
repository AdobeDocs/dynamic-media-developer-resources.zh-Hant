---
description: 僅供內部使用。 請參閱「影像呈現材料目錄參考目錄屬性」部分。
solution: Experience Manager
title: getImageRenderingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 152dfd61-2fba-47b4-8e69-fbbc8fb57f87
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 16%

---

# getImageRenderingPublishSettings{#getimagerenderingpublishsettings}

僅供內部使用。 請參閱「影像呈現材料目錄參考目錄屬性」部分。

語法

## 授權的使用者類型 {#section-1097e0563c61480a8e97822dc3527070}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-4f2cb8c589384816bb2525654ec49963}

**輸入(getImageRenderingPublishSettingsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 您要取得其影像轉譯發佈設定之公司的控制代碼。 |
| `*`contextHandle`*` | `xsd:string` | 是 | 處理發佈內容。 |

**輸出(getImageRenderingPublishSettingsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`publishSettingsArray`*` | `type:ConfigSettingArray` | 是 | 影像呈現發佈設定。 |
