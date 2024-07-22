---
description: 取代影像資產的影像資料。
solution: Experience Manager
title: replaceImage
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: bf8c1f5c-7829-4750-b5b7-b8b20d115d17
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 14%

---

# replaceImage{#replaceimage}

取代影像資產的影像資料。

語法

## 授權的使用者型別 {#section-e2aad71fb2a54612badc7b16f82ed544}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-0d0ab668fa6d4310a93fb7ef8d8dd1e0}

**輸入(replaceImageParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| companyName | `xsd:string` | 是 | 包含您要取代之影像的公司控制代碼。 |
| assetHandle | `xsd:string` | 是 | 您要取代之資產的控點。 |
| urlModifier | `xsd:string` | 是 | 產生新影像資料的「影像伺服器」命令。 |

**輸出(replaceImageReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| assetHandle | `xsd:string` | 是 | 處理新資產。 |

## 範例 {#section-cebb93576bde4cb98cb27356ca66783b}

這個程式碼範例會取代影像並套用`urlModifier`，使用指定影像伺服器不執行取代動作的命令。

**要求**

```java
<replaceImageParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetHandle>a|140626|1|102524</assetHandle>
   <urlModifier>action=none</urlModifier>
</replaceImageParam>
```

**回應**

```java
<replaceImageReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|140626|1|102524</assetHandle>
</replaceImageReturn>
```
