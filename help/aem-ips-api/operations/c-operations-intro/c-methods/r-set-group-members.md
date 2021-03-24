---
description: 設定屬於特定公司之使用者的群組成員資格。
solution: Experience Manager
title: setGroupMembers
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 9%

---


# setGroupMembers{#setgroupmembers}

設定屬於特定公司之使用者的群組成員資格。

如果您沒有完成此操作的權限，則操作會引發驗證錯誤。 如果用戶句柄陣列中的任何用戶不屬於公司句柄中指定的公司，則此情況也是正確的。

## 授權用戶類型{#section-4523594039c24aa29c8d0d5c9c415391}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-6a18562fc8e942af94be10bbb8c51151}

**輸入(setGroupMembersParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司負責人。 |
| `*`groupHandle`*` | `xsd:string` | 是 | 群組控制代碼。 |
| `*`userHandleArray`*` | `types:HandleArray` | 是 | 您要設定其群組成員資格的使用者的控制代碼陣列。 |

**輸出(setGroupMembersReturn)**

IPS API不會傳回此作業的回應。

## 範例 {#section-9c528c3f44a141ce9eaddf634f26c487}

此程式碼範例會為單一使用者設定群組成員資格。

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
