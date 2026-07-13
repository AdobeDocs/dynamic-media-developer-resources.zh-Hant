---
description: 刪除縮放目標。
solution: Experience Manager
title: Deletzoomtarget
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fa1f7cf8-038a-4fa8-b869-12ce4b2ad41f
TQID: 'https://experienceleague.adobe.com/dAO3kI0G4UM6HHSwWTqJLb0cS4gkfZi-pR-CAbknUe4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 81
ht-degree: 11%

---

# Deletzoomtarget{#deletezoomtarget}

刪除縮放目標。

## 授權的使用者型別 {#section-09ca82bc817e49048271c5cba545702e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>使用者必須擁有資產的讀寫存取權。

## 參數 {#section-225330a45e7a408f8375e084677d9cb1}

**輸入(deleteZoomTargetParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 縮放目標所屬公司的控制代碼。 |
| zoomTargetHandle | `xsd:string` | 是 | 要刪除的縮放目標控制代碼。 |

**輸出(deleteZoomTargetParam)**

IPS API未傳回此作業的回應。

## 範例 {#section-a35857a5ca884357a879f7ba6cf985fe}

此程式碼範例會從公司刪除縮放目標。

**要求**

```java
<ns1:deleteZoomTargetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:zoomTargetHandle>34194|9|301</ns1:zoomTargetHandle>
</ns1:deleteZoomTargetParam>
```

**回應**

無。

