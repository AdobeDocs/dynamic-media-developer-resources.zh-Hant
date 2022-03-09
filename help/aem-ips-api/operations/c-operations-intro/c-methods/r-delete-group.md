---
description: 刪除組。
solution: Experience Manager
title: 刪除組
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0de188de-b4b6-4f48-9918-bcf962fa9482
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 13%

---

# 刪除組{#deletegroup}

刪除組。

語法

## 授權用戶類型 {#section-ebcc67723663494db0562275b1873460}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-42775102ec724c36ae5241eea1a00b8e}

**輸入(deleteGroupParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 屬於要刪除的組的公司的句柄。 |
| 組句柄 | `xsd:string` | 是 | 要刪除的組的句柄。 |

**輸出(deleteGroupParam)**

IPS API不會為此操作返迴響應。

## 範例 {#section-8f8501af3b3348a1b5701cf9622bf6e4}

此示例代碼從公司中刪除組。 它需要一個組句柄，您必須從另一個操作中獲取該句柄。

**請求**

```java
<ns1:deleteGroupParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>241</ns1:groupHandle>
</ns1:deleteGroupParam>
```

**回答**

無。
