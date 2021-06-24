---
description: 刪除資產。
solution: Experience Manager
title: deleteAsset
feature: Dynamic Media Classic,SDK/API，資產管理
role: Developer,Administrator
exl-id: dacea36e-3d40-4aaf-94fd-f0709830caf9
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 12%

---

# deleteAsset{#deleteasset}

刪除資產。

語法

## 授權的使用者類型 {#section-e913be43b684491daf02bc73211e4290}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>使用者必須擁有資產的讀取和刪除存取權。

## 參數 {#section-0eed164e278b456fbdfb7a50727a0416}

**輸入(deleteAssetParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 資料夾所屬公司的句柄。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 要刪除的資產的控制代碼。 |

**輸出(deleteAssetParam)**

IPS API不會針對此操作傳回回應。

## 範例 {#section-d5657289f5234bb0a613dcf691507958}

此范常式式碼會從特定公司刪除任何類型的資產。 它需要資產控制代碼，您必須從其他操作取得。

**請求**

```java
<ns1:deleteAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
</ns1:deleteAssetParam>
```

**回答**

無。
