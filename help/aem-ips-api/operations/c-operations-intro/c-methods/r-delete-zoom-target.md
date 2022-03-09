---
description: 刪除縮放目標。
solution: Experience Manager
title: deleteZoomTarget
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fa1f7cf8-038a-4fa8-b869-12ce4b2ad41f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 13%

---

# deleteZoomTarget{#deletezoomtarget}

刪除縮放目標。

## 授權用戶類型 {#section-09ca82bc817e49048271c5cba545702e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用戶必須具有對資產的讀寫權限。

## 參數 {#section-225330a45e7a408f8375e084677d9cb1}

**輸入(deleteZoomTargetParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 縮放目標所屬公司的句柄。 |
| zoomTargetHandle | `xsd:string` | 是 | 要刪除的縮放目標的句柄。 |

**輸出(deleteZoomTargetParam)**

IPS API不會為此操作返迴響應。

## 範例 {#section-a35857a5ca884357a879f7ba6cf985fe}

此代碼示例從公司中刪除縮放目標。

**請求**

```java
<ns1:deleteZoomTargetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:zoomTargetHandle>34194|9|301</ns1:zoomTargetHandle>
</ns1:deleteZoomTargetParam>
```

**回答**

無。
