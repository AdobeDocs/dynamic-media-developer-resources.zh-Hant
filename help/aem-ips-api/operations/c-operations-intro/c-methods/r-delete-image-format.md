---
description: 刪除影像格式。 從saveImageFormat獲取影像格式句柄。
solution: Experience Manager
title: deleteImageFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: bd717c08-6da4-47f1-8614-e4ba79d8176c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 11%

---

# deleteImageFormat{#deleteimageformat}

刪除影像格式。 從saveImageFormat獲取影像格式句柄。

語法

## 授權的使用者類型 {#section-827e24a3019543418b0a635d46c1edfd}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-462c05d9aad746ee8d2be0656041b693}

**輸入(deleteImageFormatParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 包含您要刪除之影像格式的公司控制代碼。 |
| `*`imageFormatHandle`*` | `xsd:string` | 是 | 要刪除的影像格式的句柄。 |

**輸出(deleteImageFormatParam)**

IPS API不會針對此操作傳回回應。

## 範例 {#section-9ed9baaba13549bfaad1bc9cd7ec7009}

此程式碼範例會從公司刪除影像格式。 從其他操作獲取影像格式句柄。

**請求**

```java
<deleteImageFormatParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageFormatHandle>47|301</imageFormatHandle>
</deleteImageFormatParam>
```

**回答**

無。

**相關主題：**

[saveImageFormat](../../../operations/c-operations-intro/c-methods/r-save-image-format.md#reference-d15c27f533ef41e38b54a539a304bd1d)
