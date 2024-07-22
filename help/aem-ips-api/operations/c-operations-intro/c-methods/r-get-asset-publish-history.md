---
description: 傳回資產的發佈歷史記錄。
solution: Experience Manager
title: getAssetPublishHistory
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f337e7f9-1af6-4164-b9bd-e697548e2850
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 15%

---

# getAssetPublishHistory{#getassetpublishhistory}

傳回資產的發佈歷史記錄。

語法

## 授權的使用者型別 {#section-3b9d6a129093458fa8890139a2718912}

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
| companyHandle | `xsd:string` | 是 | 具有資產發佈歷史記錄之公司的控制代碼。 |
| assetHandle | `xsd:string` | 是 | 具有您要檢查之發佈記錄的資產。 |

**輸出(getAssetPublishHistoryReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| pubHistoryArray | `types:PublishHistoryArray` | 是 | 資產的發佈歷史記錄。 |

## 範例 {#section-53897c51e5a047c5bd5ea5a6efb2d114}

此程式碼範例會傳回資產的發佈歷史記錄。 如果伺服器傳回空白陣列，表示從未發佈資產。

**要求**

```java
<getAssetPublishHistoryParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|732|1|535</assetHandle>
</getAssetPublishHistoryParam>
```

**回應**

```java
<getAssetPublishHistoryReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <pubHistoryArray/>
</getAssetPublishHistoryReturn>
```
