---
description: 設定用戶屬性（如名稱、電子郵件、角色等）
solution: Experience Manager
title: setUserInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d8f8fe53-a874-4b77-9084-9a369862a672
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 17%

---

# setUserInfo{#setuserinfo}

設定用戶屬性（如名稱、電子郵件、角色等）

語法

## 授權用戶類型 {#section-6c28db5d15b3449492a73749e4f981ac}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-71b457921fe74acb862a1e112e550211}

**Input(setUserInfoParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| userHandle | `xsd:string` | 否 | 用戶句柄。 |
| 名字 | `xsd:string` | 是 | 名字。 |
| 姓氏 | `xsd:string` | 是 | 姓。 |
| 電子郵件 | `xsd:string` | 是 | 用戶電子郵件。 |
| 預設角色 | `xsd:string` | 是 | 設定用戶所屬每個公司中用戶的角色。 但是，請注意 `IpsAdmin` 角色將覆蓋其他每公司設定。 |
| 密碼過期 | `xsd:dateTime` | 否 | 設定的密碼到期日期。 |
| 有效 | `xsd:boolean` | 是 | 確定用戶是否是有效的IPS用戶。 |
| 成員資格陣列 | `types:CompanyMembershipUpdateArray` | 是 | 一系列公司手柄。 |

**輸出(setUserInfoReturn)**

IPS API不會為此操作返迴響應。

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
