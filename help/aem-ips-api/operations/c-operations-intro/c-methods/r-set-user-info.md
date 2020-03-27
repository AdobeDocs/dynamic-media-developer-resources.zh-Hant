---
description: 設定使用者屬性（例如名稱、電子郵件、角色等）
seo-description: 設定使用者屬性（例如名稱、電子郵件、角色等）
seo-title: setUserInfo
solution: Experience Manager
title: setUserInfo
topic: Scene7 Image Production System API
uuid: 52e3a21e-1dd5-4f9d-b460-506d280fff47
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setUserInfo{#setuserinfo}

設定使用者屬性（例如名稱、電子郵件、角色等）

語法

## 授權使用者類型 {#section-6c28db5d15b3449492a73749e4f981ac}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-71b457921fe74acb862a1e112e550211}

**輸入(setUserInfoParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`userHandle`*` | `xsd:string` | 否 | 使用者控制代碼。 |
| ` *`firstName`*` | `xsd:string` | 是 | 名字。 |
| ` *`lastName`*` | `xsd:string` | 是 | 姓氏。 |
| ` *`電子郵件`*` | `xsd:string` | 是 | 使用者電子郵件。 |
| ` *`defaultRole`*` | `xsd:string` | 是 | 為用戶所屬的每個公司設定角色。 但請注意，此角 `IpsAdmin` 色會覆寫其他每公司設定。 |
| ` *`passwordExpires`*` | `xsd:dateTime` | 否 | 設定的密碼到期日。 |
| ` *`isValid`*` | `xsd:boolean` | 是 | 確定用戶是否為有效的IPS用戶。 |
| ` *`membershArray`*` | `types:CompanyMembershipUpdateArray` | 是 | 一系列公司控制代碼。 |

**輸出(setUserInfoReturn)**

IPS API不會傳回此作業的回應。

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
