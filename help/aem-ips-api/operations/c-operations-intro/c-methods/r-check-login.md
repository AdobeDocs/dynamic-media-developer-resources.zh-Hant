---
description: 檢查具有特定公司（通過句柄標識）、電子郵件地址和密碼的用戶是否可以登錄。
solution: Experience Manager
title: checkLogin
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1f96f376-574c-464b-9c89-c215f6454b81
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 13%

---

# checkLogin{#checklogin}

檢查具有特定公司（通過句柄標識）、電子郵件地址和密碼的用戶是否可以登錄。

>[!NOTE]
>
>如果省略了公司句柄，則此方法將檢查預設用戶的登錄。

## 授權用戶類型 {#section-df8b26b550854f899948276adaca083a}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-1ad4c0b4803b4388aedd655030676cb3}

**輸入(checkLoginParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 否 | 包含用戶的公司的句柄。 |
| 電子郵件 | `xsd:string` | 是 | 用戶的電子郵件地址。 |
| 密碼 | `xsd:string` | 是 | 用戶的密碼。 |

**輸出(checkLoginParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 狀態 | `xsd:string` | 是 | 用戶登錄狀態。 |

## 範例 {#section-23f90100a9d94bc7b4045634cccd1b98}

此示例代碼使用公司句柄參數、電子郵件地址和密碼來確定用戶是否可以登錄IPS。 如果用戶 *能* 登錄，此方法返回字串， `ValidLogin`。 如果用戶 *不能* 登錄，此方法返回字串， `InvalidLogin`。

**請求**

```java
<ns1:checkLoginParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>137</ns1:companyHandle>
   <ns1:email>juser3@scene7.com</ns1:email>
   <ns1:password>welcome</ns1:password>
</ns1:checkLoginParam>
```

**回答**

```java
<ns1:checkLoginReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:status>InvalidLogin</ns1:status>
</ns1:checkLoginReturn>
```
