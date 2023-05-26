---
description: 建立使用者帳戶，並將該帳戶新增至一或多個公司。
solution: Experience Manager
title: addUser
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: aed39e73-f528-4c26-8f62-c3d796e9101a
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 13%

---

# addUser{#adduser}

建立使用者帳戶，並將該帳戶新增至一或多個公司。

將使用者新增至多個公司時，請透過公司的控點指定這些公司 `companyHandleArray`. 此操作會將控制代碼傳回給您剛剛新增的使用者。

## 授權的使用者型別 {#section-126ad42f844444fea11ecf8ad01fe1ec}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-40390a512e314b8d80ecffbb7729f6fb}

**輸入(addUserParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 名字 | `xsd:string` | 是 | 使用者的名字。 |
| 姓氏 | `xsd:string` | 是 | 使用者的姓氏。 |
| 電子郵件 | `xsd:string` | 是 | 使用者的電子郵件地址。 |
| 預設角色 | `xsd:string` | 是 | 設定使用者在其所屬每個公司中的角色。 但是請注意 `IpsAdmin` 角色會覆寫其他每個公司的設定。 |
| 密碼 | `xsd:string` | 是 | 設定使用者的密碼 |
| passwordExpires | `xsd:dateTime` | 否 | 設定密碼有效期。 傳入請求時提供時區。 時區會調整為中部時間。 |
| isValid | `xsd:boolean` | 是 | 判斷使用者是否有效。 |
| memberlationarray | `xsd:CompanyMembershipUpdateArray` | 是 | 公司控點的陣列。 |

**輸出(addUserParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| userHandle | `xsd:string` | 是 | 使用者的控制代碼。 |

## 範例 {#section-2547cef622734b71919eef849960b5cb}

IPS API會傳回指定新使用者的使用者控制代碼元素。

**請求**

```java {.line-numbers}
<ns1:addUserParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:firstName>Joe</ns1:firstName>
   <ns1:lastName>User</ns1:lastName>
   <ns1:email>juser@adobe.com</ns1:email>
   <ns1:defaultRole>TrialSiteUser</ns1:role>
   <ns1:password>passw0rd</ns1:password>
   <ns1:isValid>true</ns1:isValid>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:addUserParam>
```

**回答**

```java {.line-numbers}
<ns1:addUserReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>525s|juser@scene7.com</ns1:userHandle>
</ns1:addUserReturn>
```
