---
description: 更新影像集。
solution: Experience Manager
title: updateImageSet
feature: Dynamic Media Classic, SDK/API，影像集
role: Developer,Administrator
exl-id: d8d5fb80-17f1-424f-8a61-27189f87d603
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 18%

---

# updateImageSet{#updateimageset}

更新影像集。

語法

## 參數 {#section-3be47dbbce474ce78676b05e163492e3}

**Input(updateImageSetParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 包含要修改的影像集的公司的句柄。 |
| `*`assetHandle`*` | `xsd:string` | Ys | 要修改的影像集的控點。 |
| `*`memberArray`*` | `types:ImageSetMemberUpdateArray` | 否 | 重置映像整合員。 |
| `*`thumbAssetHandle`*` | `xsd:string` | 否 | 作為影像集縮圖的資產控點。 |

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
