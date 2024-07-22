---
description: 刪除影像地圖。
solution: Experience Manager
title: deleteImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f9942a4a-d258-4e2a-8910-44fa502d97bd
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 10%

---

# deleteImageMap{#deleteimagemap}

刪除影像地圖。

語法

## 授權的使用者型別 {#section-41fd188af16a40d4b07923165bcf15d8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>使用者必須擁有資產的讀寫存取權。

## 參數 {#section-28de12bab79045a5977c68855e37ae3d}

**輸入(deleteImageMapParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 包含要刪除之影像地圖的公司的控制代碼。 |
| imageMapHandle | `xsd:string` | 是 | 要刪除之影像地圖的控點。 |

**輸出(deleteImageMapParam)**

IPS API未傳回此作業的回應。

## 範例 {#section-b238da3332fb4e3eb3f8bda0bd6a2035}

此程式碼範例會從公司刪除影像地圖。 您必須從其他作業取得影像地圖控制代碼。

**要求**

```java
<deleteImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageMapHandle>34191|8|554</imageMapHandle>
</deleteImageMapParam>
```

**回應**

無
