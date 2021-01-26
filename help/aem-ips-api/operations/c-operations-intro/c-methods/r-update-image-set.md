---
description: 更新影像集。
seo-description: 更新影像集。
seo-title: updateImageSet
solution: Experience Manager
title: updateImageSet
topic: Dynamic Media Image Production System API
uuid: df118ba3-d86f-4005-928e-76a5a9f899fc
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 19%

---


# updateImageSet{#updateimageset}

更新影像集。

語法

## 參數 {#section-3be47dbbce474ce78676b05e163492e3}

**輸入(updateImageSetParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 包含您要修改之影像集之公司的控制代碼。 |
| `*`assetHandle`*` | `xsd:string` | Ys | 要修改的影像集的控點。 |
| `*`memberArray`*` | `types:ImageSetMemberUpdateArray` | 否 | 重設影像整合員。 |
| `*`thumbAssetHandle`*` | `xsd:string` | 否 | 當做影像集縮圖的資產控點。 |

**輸出(updateImageSetReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`序列`*` |  |  |  |

## 範例 {#section-ce47a4b6e062423fa55ed3a0fd26d7ff}

**請求**

```java
<updateImageSetParam xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <companyHandle>c|15</companyHandle> 
  <assetHandle>a|381</assetHandle> 
  <memberArray> 
    <items> 
      <assetHandle>a|374</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
    <items> 
      <assetHandle>a|375</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
    <items> 
      <assetHandle>a|376</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
  </memberArray> 
  <thumbAssetHandle>a|376</thumbAssetHandle> 
</updateImageSetParam>
```

**回答**

```java
<updateImageSetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"/>
```

