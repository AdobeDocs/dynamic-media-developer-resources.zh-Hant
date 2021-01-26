---
description: 僅供內部使用。 請參閱影像渲染材料目錄參考目錄屬性部分。
seo-description: 僅供內部使用。 請參閱影像渲染材料目錄參考目錄屬性部分。
seo-title: getImageRenderingPublishSettings
solution: Experience Manager
title: getImageRenderingPublishSettings
topic: Dynamic Media Image Production System API
uuid: b1c253b5-febe-4dc7-95a1-a5f4789030e7
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 14%

---


# getImageRenderingPublishSettings{#getimagerenderingpublishsettings}

僅供內部使用。 請參閱影像渲染材料目錄參考目錄屬性部分。

語法

## 授權用戶類型{#section-1097e0563c61480a8e97822dc3527070}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-4f2cb8c589384816bb2525654ec49963}

**輸入(getImageRenderingPublishSettingsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 您要取得其影像演算發佈設定的公司控制代碼。 |
| `*`contextHandle`*` | `xsd:string` | 是 | 處理發佈內容。 |

**輸出(getImageRenderingPublishSettingsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`publishSettingsArray`*` | `type:ConfigSettingArray` | 是 | 影像演算發佈設定。 |

