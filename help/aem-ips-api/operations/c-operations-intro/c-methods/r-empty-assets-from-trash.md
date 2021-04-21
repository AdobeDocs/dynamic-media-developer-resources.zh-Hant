---
description: 從IPS垃圾筒清空資產。
solution: Experience Manager
title: emptyAssetsFromTrash
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 7%

---


# emptyAssetsFromTrash{#emptyassetsfromtrash}

從IPS垃圾筒清空資產。

資產會存放在垃圾筒中，直到手動清空或清空垃圾筒為止。 如果手動清空，則會在垃圾筒中生存，直到最終從系統清除下一個清除作業（通常是每晚）。 如果資產超出垃圾桶，資產會作為同一清理活動的一部分被清理掉。 逾時是可設定的（預設值為7天）。

## 授權用戶類型{#section-24dee2bf5f9f4714a64955c80f2803b4}

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
| `*`companyHandle`*` | `xsd:string` | 是 | 擁有資產的公司的控制代碼。 |
| `*`assetHandleArray`*` | `types:HandleArray` | 是 | 表示要從垃圾桶清空的項目的控制點陣列。 |

**輸出(emptyAssetsFromTrashParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:Int` | 是 | 成功從垃圾桶清空的資產數。 |
| `*`warningCount`*` | `xsd:Int` | 是 | 嘗試從垃圾筒清空資產時產生的警告數。 |
| `*`errorCount`*` | `xsd:Int` | 是 | 嘗試從垃圾筒清空資產時產生的錯誤數。 |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 當操作嘗試從垃圾筒中清空資產時，產生警告的資產相關詳細資料陣列。 |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 當操作嘗試從垃圾筒中清空資產時，與產生錯誤的資產相關的詳細資訊陣列。 |

## 範例 {#section-6154a873b6c342bf92e2036280cafdcf}

此程式碼範例使用公司的控制代碼和資產控制代碼陣列，其中包含要從垃圾筒清空的資產的控制代碼。

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

