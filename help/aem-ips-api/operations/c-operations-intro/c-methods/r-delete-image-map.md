---
description: 刪除影像映射。
solution: Experience Manager
title: deleteImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f9942a4a-d258-4e2a-8910-44fa502d97bd
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 12%

---

# deleteImageMap{#deleteimagemap}

刪除影像映射。

語法

## 授權用戶類型 {#section-41fd188af16a40d4b07923165bcf15d8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用戶必須具有對資產的讀寫權限。

## 參數 {#section-28de12bab79045a5977c68855e37ae3d}

**輸入(deleteImageMapParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 包含要刪除的影像映射的公司的句柄。 |
| imageMapHandle | `xsd:string` | 是 | 要刪除的影像映射的句柄。 |

**輸出(deleteImageMapParam)**

IPS API不會為此操作返迴響應。

## 範例 {#section-b238da3332fb4e3eb3f8bda0bd6a2035}

此代碼示例從公司中刪除映像映射。 必須從其他操作獲取影像映射句柄。

**請求**

```java
<deleteImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageMapHandle>34191|8|554</imageMapHandle>
</deleteImageMapParam>
```

**回答**

無
