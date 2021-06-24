---
description: 從IPS垃圾桶清空資產。
solution: Experience Manager
title: emptyAssetsFromTrash
feature: Dynamic Media Classic,SDK/API，資產管理
role: Developer,Administrator
exl-id: 36866dc8-6a16-4445-942f-d0ea3c168272
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 7%

---

# emptyAssetsFromTrash{#emptyassetsfromtrash}

從IPS垃圾桶清空資產。

資產會存放在垃圾桶中，直到手動清空，或直到超出垃圾桶。 如果手動清空，則會存放在垃圾桶中，直到下次清除工作（通常是每晚），當它們最終從系統清除時。 如果資產超時從垃圾桶中清除，則會作為相同清除活動的一部分清除資產。 逾時是可設定的（預設值為7天）。

## 授權的使用者類型 {#section-24dee2bf5f9f4714a64955c80f2803b4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* &quot;

## 參數 {#section-8e1fb0ee3aae453581e99ef76e298569}

**輸入(emptyAssetsFromTrashParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 擁有資產的公司的控制方。 |
| `*`assetHandleArray`*` | `types:HandleArray` | 是 | 表示要從垃圾清空的項目的句柄陣列。 |

**輸出(emptyAssetsFromTrashParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:Int` | 是 | 成功從垃圾桶清空的資產數。 |
| `*`warningCount`*` | `xsd:Int` | 是 | 操作嘗試從垃圾桶清空資產時產生的警告數。 |
| `*`errorCount`*` | `xsd:Int` | 是 | 操作嘗試從清單中清空資產時產生的錯誤數。 |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 與資產相關聯的詳細資料陣列，當操作嘗試從垃圾桶中清空資產時，資產會產生警告。 |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 與當操作嘗試從垃圾桶清空資產時產生錯誤的資產相關聯的詳細資料陣列。 |

## 範例 {#section-6154a873b6c342bf92e2036280cafdcf}

此程式碼範例使用公司的控制代碼和資產控制代碼陣列，其中包含要從垃圾桶清空的資產的控制代碼。

**請求**

```java
<emptyAssetsFromTrashParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</emptyAssetsFromTrashParam>
```

**回答**

```java
<emptyAssetsFromTrashReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</emptyAssetsFromTrashReturn>
```
