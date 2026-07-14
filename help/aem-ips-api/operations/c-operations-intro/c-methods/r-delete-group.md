---
description: 刪除群組。
solution: Experience Manager
title: deleteGroup
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0de188de-b4b6-4f48-9918-bcf962fa9482
TQID: 'https://experienceleague.adobe.com/skfJjk-dexrQR94ImWtaWV-1hkPmvrlFVn-EyA5mKtQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 86
ht-degree: 11%

---

# deleteGroup{#deletegroup}

刪除群組。

語法

## 授權的使用者型別 {#section-ebcc67723663494db0562275b1873460}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-42775102ec724c36ae5241eea1a00b8e}

**輸入(deleteGroupParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 屬於您要刪除之群組之公司的控制代碼。 |
| groupHandle | `xsd:string` | 是 | 您要刪除之群組的控制代碼。 |

**輸出(deleteGroupParam)**

IPS API未傳回此作業的回應。

## 範例 {#section-8f8501af3b3348a1b5701cf9622bf6e4}

這個程式碼範例會從公司中刪除群組。 它需要群組控制代碼，您必須從其他作業取得此控制代碼。

**要求**

```java
<ns1:deleteGroupParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>241</ns1:groupHandle>
</ns1:deleteGroupParam>
```

**回應**

無。

