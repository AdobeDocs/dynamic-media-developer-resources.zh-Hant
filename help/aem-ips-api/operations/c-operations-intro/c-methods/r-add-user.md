---
description: 建立使用者帳戶，並將該帳戶新增至一或多個公司。
solution: Experience Manager
title: addUser
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: aed39e73-f528-4c26-8f62-c3d796e9101a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 12%

---

# addUser{#adduser}

建立使用者帳戶，並將該帳戶新增至一或多個公司。

將使用者新增至多個公司時，請在`companyHandleArray`中依公司控點指定這些公司。 此操作將句柄返回給您剛添加的用戶。

## 授權的使用者類型 {#section-126ad42f844444fea11ecf8ad01fe1ec}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-40390a512e314b8d80ecffbb7729f6fb}

**輸入(addUserParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`firstName`*` | `xsd:string` | 是 | 使用者的名字。 |
| `*`lastName`*` | `xsd:string` | 是 | 使用者的姓氏。 |
| `*`電子郵件`*` | `xsd:string` | 是 | 使用者的電子郵件地址。 |
| `*`defaultRole`*` | `xsd:string` | 是 | 設定使用者所屬每個公司中的角色。 但請注意，`IpsAdmin`角色會覆寫其他每公司設定。 |
| `*`密碼`*` | `xsd:string` | 是 | 設定使用者的密碼 |
| `*`passwordExpires`*` | `xsd:dateTime` | 否 | 設定密碼過期時間。 傳入要求時提供時區。 時區會調整為中央時間。 |
| `*`isValid`*` | `xsd:boolean` | 是 | 確定用戶是否有效。 |
| `*`membershipArray`*` | `xsd:CompanyMembershipUpdateArray` | 是 | 公司控制代碼的陣列。 |

**輸出(addUserParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | 是 | 使用者的控制代碼。 |

## 範例 {#section-2547cef622734b71919eef849960b5cb}

IPS API返回指定新用戶的用戶句柄元素。

**請求**

```java
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

```java
<ns1:addUserReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>525s|juser@scene7.com</ns1:userHandle>
</ns1:addUserReturn>
```
