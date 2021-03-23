---
description: 取代影像資產的影像資料。
seo-description: 取代影像資產的影像資料。
seo-title: replaceImage
solution: Experience Manager
title: replaceImage
uuid: 46824e33-265c-4425-9ab1-8ad6b7ac154d
feature: Dynamic Media經典，SDK/API，資產管理
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 14%

---


# replaceImage{#replaceimage}

取代影像資產的影像資料。

語法

## 授權用戶類型{#section-e2aad71fb2a54612badc7b16f82ed544}

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
| `*`companyName`*` | `xsd:string` | 是 | 包含您要取代之影像的公司控制代碼。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 您要取代之資產的控制代碼。 |
| `*`urlModifier`*` | `xsd:string` | 是 | 產生新影像資料的影像伺服器指令。 |

**輸出(replaceImageReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | 是 | 處理新資產。 |

## 範例 {#section-cebb93576bde4cb98cb27356ca66783b}

此程式碼範例會取代影像，並套用`urlModifier`命令，指定影像伺服器在取代時不會採取任何動作。

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

