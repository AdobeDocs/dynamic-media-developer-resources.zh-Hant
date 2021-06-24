---
description: 取代影像資產的影像資料。
solution: Experience Manager
title: replaceImage
feature: Dynamic Media Classic,SDK/API，資產管理
role: Developer,Administrator
exl-id: bf8c1f5c-7829-4750-b5b7-b8b20d115d17
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 15%

---

# replaceImage{#replaceimage}

取代影像資產的影像資料。

語法

## 授權的使用者類型 {#section-e2aad71fb2a54612badc7b16f82ed544}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-0d0ab668fa6d4310a93fb7ef8d8dd1e0}

**Input(replaceImageParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyName`*` | `xsd:string` | 是 | 用要替換的影像處理公司。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 您要替換的資產的控點。 |
| `*`urlModifier`*` | `xsd:string` | 是 | 生成新映像資料的映像伺服器命令。 |

**輸出(replaceImageReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | 是 | 處理新資產。 |

## 範例 {#section-cebb93576bde4cb98cb27356ca66783b}

此程式碼範例會取代影像，並使用指定影像伺服器在取代時不會採取任何動作的命令來套用`urlModifier`。

**請求**

```java
<replaceImageParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetHandle>a|140626|1|102524</assetHandle>
   <urlModifier>action=none</urlModifier>
</replaceImageParam>
```

**回答**

```java
<replaceImageReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|140626|1|102524</assetHandle>
</replaceImageReturn>
```
