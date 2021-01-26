---
description: 傳回資產的發佈歷史記錄。
seo-description: 傳回資產的發佈歷史記錄。
seo-title: getAssetPublishHistory
solution: Experience Manager
title: getAssetPublishHistory
topic: Dynamic Media Image Production System API
uuid: 15025c3d-eac3-4cb8-9a2a-fd80bd67478f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 16%

---


# getAssetPublishHistory{#getassetpublishhistory}

傳回資產的發佈歷史記錄。

語法

## 授權用戶類型{#section-3b9d6a129093458fa8890139a2718912}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-3541bd9914a44b89acfc1d419b560ee6}

**輸入(getAssetPublishHistoryParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 具有資產發佈歷史記錄的公司的控制代碼。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 您要檢查具有發佈歷史記錄的資產。 |

**輸出(getAssetPublishHistoryReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`pubHistoryArray`*` | `types:PublishHistoryArray` | 是 | 資產的發佈歷史記錄。 |

## 範例 {#section-53897c51e5a047c5bd5ea5a6efb2d114}

此程式碼範例會傳回資產的發佈歷史記錄。 如果伺服器傳回空的陣列，則資產從未發佈。

**請求**

```java
<getAssetPublishHistoryParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|732|1|535</assetHandle>
</getAssetPublishHistoryParam>
```

**回答**

```java
<getAssetPublishHistoryReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <pubHistoryArray/>
</getAssetPublishHistoryReturn>
```

