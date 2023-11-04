---
description: 設定使用者屬性（例如名稱、電子郵件、角色等）。
solution: Experience Manager
title: setUserInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d8f8fe53-a874-4b77-9084-9a369862a672
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 16%

---

# setUserInfo{#setuserinfo}

設定使用者屬性（例如名稱、電子郵件、角色等）。

語法

## 授權的使用者型別 {#section-6c28db5d15b3449492a73749e4f981ac}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-71b457921fe74acb862a1e112e550211}

**輸入(setUserInfoParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| userHandle | `xsd:string` | 否 | 使用者控制代碼。 |
| 名字 | `xsd:string` | 是 | 名字。 |
| 姓氏 | `xsd:string` | 是 | 姓氏。 |
| 電子郵件 | `xsd:string` | 是 | 使用者電子郵件。 |
| defaultrole | `xsd:string` | 是 | 設定使用者在其所屬每個公司中的角色。 但是，請注意 `IpsAdmin` 角色會覆寫其他每個公司的設定。 |
| 密碼過期 | `xsd:dateTime` | 否 | 設定的密碼到期日。 |
| isValid | `xsd:boolean` | 是 | 判斷使用者是否為有效的IPS使用者。 |
| memberlationarray | `types:CompanyMembershipUpdateArray` | 是 | 公司控制元件的陣列。 |

**輸出(setUserInfoReturn)**

IPS API未傳回此作業的回應。

## 範例 {#section-272c103076fb4de0a53729e2f6bfb895}

**請求**

```java
<setUserInfoParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <firstName>test</firstName>
   <lastName>test</lastName>
   <email>test@test.test</email>
   <defaultRole>IpsAdmin</defaultRole>
   <isValid>true</isValid>
</setUserInfoParam>
```

**回答**

無。
