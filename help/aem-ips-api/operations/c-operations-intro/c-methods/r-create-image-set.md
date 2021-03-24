---
description: 建立影像集。
solution: Experience Manager
title: createImageSet
feature: Dynamic Media經典，SDK/API，影像集
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 13%

---


# createImageSet{#createimageset}

建立影像集。

語法

## 授權用戶類型{#section-58bf5027e6d24ab5a9fcba59776d15dc}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用戶必須具有對目標資料夾的讀／寫訪問權限。

## 參數 {#section-03d22ba7d290477e91c25ca1d4439200}

**輸入(createImageSetParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 影像集所屬公司的控制代碼。 |
| `*`folderHandle`*` | `xsd:string` | 是 | 資料夾的句柄。 |
| `*`名稱`*` | `xsd:string` | 是 | 影像集名稱。 |
| `*`類型`*` | `xsd:string` | 是 | 影像集類型。 |
| `*`thumbAssetHandle`*` | `xsd:string` | 否 | 當做新影像集縮圖的資產控制代碼。 如果未指定，IPS會嘗試使用該集所引用的第一個映像資產。 |

**輸出**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | 是 | 新影像集的控點。 |

## 範例 {#section-385fe3b0af8044b0a2451336ec137fc5}

此程式碼範例會建立由公司、資料夾、名稱和類型指定的影像集。 回應是新建影像集的資產控制代碼。

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

