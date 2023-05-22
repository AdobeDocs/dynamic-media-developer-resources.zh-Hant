---
description: 建立影像集。
solution: Experience Manager
title: 建立影像集
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 01ccc705-97e4-4e75-a322-e24bb78cb496
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 15%

---

# 建立影像集{#createimageset}

建立影像集。

語法

## 授權用戶類型 {#section-58bf5027e6d24ab5a9fcba59776d15dc}

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
| 公司句柄 | `xsd:string` | 是 | 映像集所屬公司的句柄。 |
| folderHandle | `xsd:string` | 是 | 資料夾的句柄。 |
| name | `xsd:string` | 是 | 影像集名稱。 |
| type | `xsd:string` | 是 | 影像集類型。 |
| 拇指資產句柄 | `xsd:string` | 否 | 用作新影像集縮略圖的資產的句柄。 如果未指定，IPS將嘗試使用該集引用的第一個影像資源。 |

**輸出**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 資產句柄 | `xsd:string` | 是 | 新影像集的句柄。 |

## 範例 {#section-385fe3b0af8044b0a2451336ec137fc5}

此代碼示例建立由公司、資料夾、名稱和類型指定的映像集。 響應是新建立的映像集的資產句柄。

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
