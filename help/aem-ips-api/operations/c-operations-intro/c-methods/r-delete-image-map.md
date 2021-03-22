---
description: 刪除影像地圖。
seo-description: 刪除影像地圖。
seo-title: deleteImageMap
solution: Experience Manager
title: deleteImageMap
uuid: 0abdf72c-f445-41d0-bd88-63b7ad1359d5
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 11%

---


# deleteImageMap{#deleteimagemap}

刪除影像地圖。

語法

## 授權用戶類型{#section-41fd188af16a40d4b07923165bcf15d8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>使用者必須擁有資產的讀取和寫入存取權。

## 參數 {#section-28de12bab79045a5977c68855e37ae3d}

**輸入(deleteImageMapParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 包含要刪除之影像地圖之公司的控制代碼。 |
| `*`imageMapHandle`*` | `xsd:string` | 是 | 要刪除的影像地圖的控點。 |

**輸出(deleteImageMapParam)**

IPS API不會傳回此作業的回應。

## 範例 {#section-b238da3332fb4e3eb3f8bda0bd6a2035}

此程式碼範例會從公司刪除影像地圖。 您必須從其他操作獲取影像映射句柄。

**請求**

```java
<deleteImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageMapHandle>34191|8|554</imageMapHandle>
</deleteImageMapParam>
```

**回答**

無
