---
description: 刪除影像地圖。
solution: Experience Manager
title: deleteImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: f9942a4a-d258-4e2a-8910-44fa502d97bd
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 12%

---

# deleteImageMap{#deleteimagemap}

刪除影像地圖。

語法

## 授權的使用者類型 {#section-41fd188af16a40d4b07923165bcf15d8}

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
| `*`companyHandle`*` | `xsd:string` | 是 | 包含要刪除之影像對映的公司控制代碼。 |
| `*`imageMapHandle`*` | `xsd:string` | 是 | 要刪除的影像映射的句柄。 |

**輸出(deleteImageMapParam)**

IPS API不會針對此操作傳回回應。

## 範例 {#section-b238da3332fb4e3eb3f8bda0bd6a2035}

此程式碼範例會從公司刪除影像對應。 您必須從其他操作獲取影像映射句柄。

**請求**

```java
<deleteImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageMapHandle>34191|8|554</imageMapHandle>
</deleteImageMapParam>
```

**回答**

無
