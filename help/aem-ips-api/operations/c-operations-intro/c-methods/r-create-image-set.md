---
description: 建立影像集。
solution: Experience Manager
title: createImageSet
feature: Dynamic Media Classic, SDK/API，影像集
role: Developer,Administrator
exl-id: 01ccc705-97e4-4e75-a322-e24bb78cb496
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 13%

---

# createImageSet{#createimageset}

建立影像集。

語法

## 授權的使用者類型 {#section-58bf5027e6d24ab5a9fcba59776d15dc}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用戶必須具有對目標資料夾的讀/寫訪問權限。

## 參數 {#section-03d22ba7d290477e91c25ca1d4439200}

**輸入(createImageSetParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 影像集所屬公司的控制代碼。 |
| `*`folderHandle`*` | `xsd:string` | 是 | 資料夾的控點。 |
| `*`名稱`*` | `xsd:string` | 是 | 影像集名稱。 |
| `*`類型`*` | `xsd:string` | 是 | 影像集類型。 |
| `*`thumbAssetHandle`*` | `xsd:string` | 否 | 作為新影像集縮圖的資產處理。 如果未指定，IPS會嘗試使用由集引用的第一個影像資產。 |

**輸出**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | 是 | 新影像集的控點。 |

## 範例 {#section-385fe3b0af8044b0a2451336ec137fc5}

此程式碼範例會建立由公司、資料夾、名稱和類型指定的影像集。 回應是新建立之影像集的資產控制代碼。

**請求**

```java
<ns1:createImageSetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/eCatalogs/</ns1:folderHandle>
   <ns1:name>My Image Set</ns1:name>
   <ns1:type>ImageSet</ns1:type>
</ns1:createImageSetParam>
```

**回答**

```java
<createImageSetReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <assetHandle>25741|22|841</assetHandle>
</createImageSetReturn>
```
