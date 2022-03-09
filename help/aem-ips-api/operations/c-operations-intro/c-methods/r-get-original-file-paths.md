---
description: 獲取公司資產的原始檔案路徑。
solution: Experience Manager
title: getOriginalFilePaths
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 81d06a8c-55c1-47d5-adc9-928ab30199c6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 16%

---

# getOriginalFilePaths{#getoriginalfilepaths}

獲取公司資產的原始檔案路徑。

語法

## 授權用戶類型 {#section-da8d8561e9174e938f3595a5d6e50089}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>需要對資產的讀權限。

## 參數 {#section-a6b394daba6e49a8882cf3051035d9d1}

**輸入(getOriginalFilePathsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 公司的把手。 |
| assetHandleArray | `types:HandleArray` | 是 | 要獲取其原始檔案路徑的資產的句柄陣列。 |

**輸出(getOriginalFilePathsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 原始檔案陣列 | `types:StringArray` | 是 | 表示原始檔案路徑的字串陣列。 |

## 範例 {#section-a966e783a2ba49f5b6b0f961329ab2f8}

此代碼示例返回資產句柄陣列中使用唯一資產句柄指定的資產的檔案路徑。

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
