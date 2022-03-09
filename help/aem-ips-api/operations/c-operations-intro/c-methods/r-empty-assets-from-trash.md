---
title: 空AssetsFromTrash
description: 從IPS垃圾中清空資產。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 36866dc8-6a16-4445-942f-d0ea3c168272
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 8%

---

# 空AssetsFromTrash{#emptyassetsfromtrash}

從IPS垃圾中清空資產。

資產會一直存在垃圾中，直到被人工清空，或者衝出垃圾。 如果手動清空這些檔案，則它們會一直存在「垃圾」中，直到下一個清理作業（通常每晚）才從系統中清除。 如果他們超時清理垃圾，資產會被清理，作為同一清理活動的一部分。 超時是可配置的（預設值為7天）。

## 授權用戶類型 {#section-24dee2bf5f9f4714a64955c80f2803b4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-8e1fb0ee3aae453581e99ef76e298569}

**輸入(emptyAssetsFromTrashParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | xsd:string | 是 | 擁有資產的公司的手柄。 |
| assetHandleArray | 類型：HandleArray | 是 | 表示要從垃圾中清空的物品的手柄陣列。 |

**輸出(emptyAssetsFromTrashParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 成功計數 | xsd:Int | 是 | 成功從垃圾箱清空的資產數。 |
| 警告計數 | xsd:Int | 是 | 操作嘗試從垃圾箱清空資產時生成的警告數。 |
| 錯誤計數 | xsd:Int | 是 | 操作嘗試從垃圾站清空資產時生成的錯誤數。 |
| 警告DetailArray | 類型：AssetOperationFaultArray | 否 | 與操作嘗試從垃圾箱清空時生成警告的資產關聯的詳細資訊陣列。 |
| 錯誤DetailArray | 類型：AssetOperationFaultArray | 否 | 與操作嘗試從垃圾箱清空時生成錯誤的資產關聯的詳細資訊陣列。 |

## 範例 {#section-6154a873b6c342bf92e2036280cafdcf}

此代碼示例使用公司的句柄和資產句柄陣列，該陣列包含要從垃圾箱清空的資產的句柄。

**請求**

```java
<emptyAssetsFromTrashParam xmlns="http://www.scene7.com/IpsApi/xsd/2023-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</emptyAssetsFromTrashParam>
```

**回答**

```java
<emptyAssetsFromTrashReturn xmlns="http://www.scene7.com/IpsApi/xsd/2023-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</emptyAssetsFromTrashReturn>
```
