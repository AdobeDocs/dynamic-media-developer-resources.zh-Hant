---
description: 設定屬於特定公司的用戶的組成員身份。
solution: Experience Manager
title: setGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 81348da7-6733-4da9-8a0a-376fccf791ea
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 9%

---

# setGroupMembers{#setgroupmembers}

設定屬於特定公司的用戶的組成員身份。

如果您沒有完成此操作的權限，該操作將引發身份驗證錯誤。 如果用戶句柄陣列中的任何用戶不屬於公司句柄中指定的公司，則也會出現這種情況。

## 授權用戶類型 {#section-4523594039c24aa29c8d0d5c9c415391}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-6a18562fc8e942af94be10bbb8c51151}

**Input(setGroupMembersParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 公司負責。 |
| 組句柄 | `xsd:string` | 是 | 組句柄。 |
| userHandleArray | `types:HandleArray` | 是 | 要設定其組成員身份的用戶的句柄陣列。 |

**輸出(setGroupMembesReturn)**

IPS API不會為此操作返迴響應。

## 範例 {#section-9c528c3f44a141ce9eaddf634f26c487}

此代碼示例為單個用戶設定組成員身份。

**請求**

```java
<ns1:setGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
   <ns1:userHandleArray>
      <ns1:items>70|kmagnusson@adobe.com</ns1:items>
   </ns1:userHandleArray>
</ns1:setGroupMembersParam>
```

**回答**

無。
