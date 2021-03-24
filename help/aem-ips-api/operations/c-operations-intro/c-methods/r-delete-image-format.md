---
description: 刪除影像格式。 從saveImageFormat取得影像格式控制代碼。
solution: Experience Manager
title: deleteImageFormat
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 11%

---


# deleteImageFormat{#deleteimageformat}

刪除影像格式。 從saveImageFormat取得影像格式控制代碼。

語法

## 授權用戶類型{#section-827e24a3019543418b0a635d46c1edfd}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-462c05d9aad746ee8d2be0656041b693}

**輸入(deleteImageFormatParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 包含您要刪除之影像格式之公司的控制代碼。 |
| `*`imageFormatHandle`*` | `xsd:string` | 是 | 要刪除的影像格式的句柄。 |

**輸出(deleteImageFormatParam)**

IPS API不會傳回此作業的回應。

## 範例 {#section-9ed9baaba13549bfaad1bc9cd7ec7009}

此程式碼範例會從公司刪除影像格式。 從另一個操作獲取影像格式句柄。

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
