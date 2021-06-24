---
description: 刪除縮放目標。
solution: Experience Manager
title: deleteZoomTarget
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: fa1f7cf8-038a-4fa8-b869-12ce4b2ad41f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 12%

---

# deleteZoomTarget{#deletezoomtarget}

刪除縮放目標。

## 授權的使用者類型 {#section-09ca82bc817e49048271c5cba545702e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>使用者必須擁有資產的讀取和寫入存取權。

## 參數 {#section-225330a45e7a408f8375e084677d9cb1}

**輸入(deleteZoomTargetParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 縮放目標所屬公司的控制代碼。 |
| `*`zoomTargetHandle`*` | `xsd:string` | 是 | 要刪除的縮放目標的控制代碼。 |

**輸出(deleteZoomTargetParam)**

IPS API不會針對此操作傳回回應。

## 範例 {#section-a35857a5ca884357a879f7ba6cf985fe}

此程式碼範例會刪除公司中的縮放目標。

**請求**

```java
<ns1:deleteZoomTargetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:zoomTargetHandle>34194|9|301</ns1:zoomTargetHandle>
</ns1:deleteZoomTargetParam>
```

**回答**

無。
