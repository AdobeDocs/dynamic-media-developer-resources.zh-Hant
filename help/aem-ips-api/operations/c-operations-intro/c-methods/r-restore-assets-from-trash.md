---
description: 從垃圾箱中恢復資產。
solution: Experience Manager
title: restoreAssetsFromTrash
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: b1cde1a9-d726-4ebc-9d49-ee72a6b56fc9
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 12%

---

# restoreAssetsFromTrash{#restoreassetsfromtrash}

從垃圾箱中恢復資產。

語法

## 授權用戶類型 {#section-15e887782c7d4ace897ff02c6ad5baa0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-200a61d040c94e489a85241b29cd499a}

**輸入(restoreAssetsFromTrashParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 要恢復資產的公司的句柄。 |
| assetHandleArray | `types:HandleArray` | 是 | 要恢復的資產的句柄陣列。 |

**輸出(restoreAssetsFromTrashReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 成功計數 | `xsd:int` | 是 | 成功從垃圾箱中刪除的資產數。 |
| 警告計數 | `xsd:int` | 是 | 操作嘗試從垃圾站還原資產時生成的警告數。 |
| 錯誤計數 | `xsd:int` | 是 | 嘗試從垃圾站還原資產時生成的錯誤數。 |
| 警告DetailArray | `types:AssetOperationFaultArray` | 否 | 與在操作嘗試從垃圾箱還原資產時生成警告的資產關聯的詳細資訊陣列。 |
| 錯誤DetailArray | `types:AssetOperationFaultArray` | 否 | 與在操作嘗試從垃圾箱還原資產時生成錯誤的資產關聯的詳細資訊陣列。 |

## 範例 {#section-98fe0394b0634ca397c395f14f8a9358}

此代碼示例從垃圾箱中恢復資產。 響應指示操作已成功完成。

**請求**

```java
<restoreAssetsFromTrashParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</restoreAssetsFromTrashParam>
```

**回答**

```java
<restoreAssetsFromTrashReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</restoreAssetsFromTrashReturn
```
