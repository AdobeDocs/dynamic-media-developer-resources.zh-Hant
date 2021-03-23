---
description: 刪除群組。
seo-description: 刪除群組。
seo-title: deleteGroup
solution: Experience Manager
title: deleteGroup
uuid: 04934b16-b7ef-4657-9f63-c91fcc741ca4
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 12%

---


# deleteGroup{#deletegroup}

刪除群組。

語法

## 授權用戶類型{#section-ebcc67723663494db0562275b1873460}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-42775102ec724c36ae5241eea1a00b8e}

**輸入(deleteGroupParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 屬於您要刪除之群組的公司控制代碼。 |
| `*`groupHandle`*` | `xsd:string` | 是 | 要刪除的組的句柄。 |

**輸出(deleteGroupParam)**

IPS API不會傳回此作業的回應。

## 範例 {#section-8f8501af3b3348a1b5701cf9622bf6e4}

此范常式式碼會從公司中刪除群組。 它需要一個組句柄，您必須從其他操作中獲得該句柄。

**請求**

```java
<ns1:deleteGroupParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>241</ns1:groupHandle>
</ns1:deleteGroupParam>
```

**回答**

無。
