---
description: 取得公司資產的原始檔案路徑。
solution: Experience Manager
title: getOriginalFilePaths
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 81d06a8c-55c1-47d5-adc9-928ab30199c6
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 15%

---

# getOriginalFilePaths{#getoriginalfilepaths}

取得公司資產的原始檔案路徑。

語法

## 授權的使用者類型 {#section-da8d8561e9174e938f3595a5d6e50089}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>需要資產的讀取存取權。

## 參數 {#section-a6b394daba6e49a8882cf3051035d9d1}

**輸入(getOriginalFilePathsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司的把手。 |
| `*`assetHandleArray`*` | `types:HandleArray` | 是 | 要取得原始檔案路徑的資產的控點陣列。 |

**輸出(getOriginalFilePathsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`originalFileArray`*` | `types:StringArray` | 是 | 代表原始檔案路徑的字串陣列。 |

## 範例 {#section-a966e783a2ba49f5b6b0f961329ab2f8}

此程式碼範例會傳回資產控制代碼陣列中，以唯一資產控制代碼指定之資產的檔案路徑。

**請求**

```java
<ns1:getOriginalFilePathsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandleArray>
      <ns1:items>24265|1|17061</ns1:items>
      <ns1:items>24267|1|17063</ns1:items>
   </ns1:assetHandleArray>
</ns1:getOriginalFilePathsParam>
```

**回答**

```java
<getOriginalFilePathsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <originalFileArray>
      <items>MyCompany/Autumn Leaves.jpg</items>
      <items>MyCompany/Desert Landscape.jpg</items>
   </originalFileArray>
</getOriginalFilePathsReturn>
```
