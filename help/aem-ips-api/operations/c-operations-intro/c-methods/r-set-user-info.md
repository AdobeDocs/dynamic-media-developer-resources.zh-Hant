---
description: 設定使用者屬性（例如名稱、電子郵件、角色等）
solution: Experience Manager
title: setUserInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: d8f8fe53-a874-4b77-9084-9a369862a672
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 16%

---

# setUserInfo{#setuserinfo}

設定使用者屬性（例如名稱、電子郵件、角色等）

語法

## 授權的使用者類型 {#section-6c28db5d15b3449492a73749e4f981ac}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-71b457921fe74acb862a1e112e550211}

**輸入(setUserInfoParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | 否 | 用戶句柄。 |
| `*`firstName`*` | `xsd:string` | 是 | 名字。 |
| `*`lastName`*` | `xsd:string` | 是 | 姓氏。 |
| `*`電子郵件`*` | `xsd:string` | 是 | 使用者電子郵件。 |
| `*`defaultRole`*` | `xsd:string` | 是 | 設定使用者所屬每個公司中的角色。 但請注意，`IpsAdmin`角色會覆寫其他每公司設定。 |
| `*`passwordExpires`*` | `xsd:dateTime` | 否 | 設定密碼的到期日期。 |
| `*`isValid`*` | `xsd:boolean` | 是 | 確定用戶是否為有效的IPS用戶。 |
| `*`membershipArray`*` | `types:CompanyMembershipUpdateArray` | 是 | 公司控制代碼的陣列。 |

**輸出(setUserInfoReturn)**

IPS API不會針對此操作傳回回應。

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
