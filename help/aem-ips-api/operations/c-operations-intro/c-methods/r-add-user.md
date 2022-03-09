---
description: 建立用戶帳戶並將該帳戶添加到一個或多個公司。
solution: Experience Manager
title: addUser
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: aed39e73-f528-4c26-8f62-c3d796e9101a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 13%

---

# addUser{#adduser}

建立用戶帳戶並將該帳戶添加到一個或多個公司。

將用戶添加到多個公司時，按公司句柄指定這些公司 `companyHandleArray`。 此操作將句柄返回給您剛添加的用戶。

## 授權用戶類型 {#section-126ad42f844444fea11ecf8ad01fe1ec}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-40390a512e314b8d80ecffbb7729f6fb}

**Input(addUserParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 名字 | `xsd:string` | 是 | 用戶的名字。 |
| 姓氏 | `xsd:string` | 是 | 用戶的姓。 |
| 電子郵件 | `xsd:string` | 是 | 用戶的電子郵件地址。 |
| 預設角色 | `xsd:string` | 是 | 設定用戶所屬每個公司中用戶的角色。 但是，請注意 `IpsAdmin` 角色將覆蓋其他每公司設定。 |
| 密碼 | `xsd:string` | 是 | 設定用戶密碼 |
| 密碼過期 | `xsd:dateTime` | 否 | 設定密碼到期期。 在傳遞請求時提供時區。 將時區調整為「中央時間」。 |
| 有效 | `xsd:boolean` | 是 | 確定用戶是否有效。 |
| 成員資格陣列 | `xsd:CompanyMembershipUpdateArray` | 是 | 一系列公司手柄。 |

**輸出(addUserParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| userHandle | `xsd:string` | 是 | 用戶的句柄。 |

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
