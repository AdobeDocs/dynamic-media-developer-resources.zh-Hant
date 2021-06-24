---
description: 從垃圾桶還原資產。
solution: Experience Manager
title: restoreAssetsFromTrash
feature: Dynamic Media Classic,SDK/API，資產管理
role: Developer,Administrator
exl-id: b1cde1a9-d726-4ebc-9d49-ee72a6b56fc9
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 12%

---

# restoreAssetsFromTrash{#restoreassetsfromtrash}

從垃圾桶還原資產。

語法

## 授權的使用者類型 {#section-15e887782c7d4ace897ff02c6ad5baa0}

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
| `*`companyHandle`*` | `xsd:string` | 是 | 含有您要還原之資產的公司控制代碼。 |
| `*`assetHandleArray`*` | `types:HandleArray` | 是 | 您要還原之資產的控點陣列。 |

**輸出(restoreAssetsFromTrashReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | 是 | 成功從垃圾桶移除的資產數。 |
| `*`warningCount`*` | `xsd:int` | 是 | 嘗試從清單還原資產時產生的警告數。 |
| `*`errorCount`*` | `xsd:int` | 是 | 嘗試從清單還原資產時產生的錯誤數。 |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 與資產相關聯的詳細資訊陣列，當操作嘗試從垃圾桶還原資產時，資產會產生警告。 |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 與資產相關聯的詳細資訊陣列，當操作嘗試從清單還原資產時，資產會產生錯誤。 |

## 範例 {#section-98fe0394b0634ca397c395f14f8a9358}

此程式碼範例會從垃圾桶還原資產。 響應指示操作已成功完成。

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
