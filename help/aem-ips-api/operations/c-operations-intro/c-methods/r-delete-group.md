---
description: 刪除群組。
solution: Experience Manager
title: deleteGroup
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 0de188de-b4b6-4f48-9918-bcf962fa9482
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 13%

---

# deleteGroup{#deletegroup}

刪除群組。

語法

## 授權的使用者類型 {#section-ebcc67723663494db0562275b1873460}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-42775102ec724c36ae5241eea1a00b8e}

**輸入(deleteGroupParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 屬於您要刪除之群組的公司的控制代碼。 |
| `*`groupHandle`*` | `xsd:string` | 是 | 要刪除的組的句柄。 |

**輸出(deleteGroupParam)**

IPS API不會針對此操作傳回回應。

## 範例 {#section-8f8501af3b3348a1b5701cf9622bf6e4}

此范常式式碼會從公司中刪除群組。 它需要組句柄，您必須從其他操作中獲取該句柄。

**請求**

```java
<ns1:deleteGroupParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>241</ns1:groupHandle>
</ns1:deleteGroupParam>
```

**回答**

無。
