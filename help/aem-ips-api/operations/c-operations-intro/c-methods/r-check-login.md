---
description: 檢查具有特定公司（由控制代碼識別）、電子郵件地址和密碼的使用者是否可以登入。
solution: Experience Manager
title: checkLogin
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 1f96f376-574c-464b-9c89-c215f6454b81
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 12%

---

# checkLogin{#checklogin}

檢查具有特定公司（由控制代碼識別）、電子郵件地址和密碼的使用者是否可以登入。

>[!NOTE]
>
>如果省略公司控制代碼，此方法會檢查預設使用者的登入。

## 授權的使用者類型 {#section-df8b26b550854f899948276adaca083a}

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
| `*`companyHandle`*` | `xsd:string` | 否 | 包含使用者之公司的控制代碼。 |
| `*`電子郵件`*` | `xsd:string` | 是 | 使用者的電子郵件地址。 |
| `*`密碼`*` | `xsd:string` | 是 | 使用者的密碼。 |

**輸出(checkLoginParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`狀態`*` | `xsd:string` | 是 | 使用者的登入狀態。 |

## 範例 {#section-23f90100a9d94bc7b4045634cccd1b98}

此范常式式碼使用公司控制代碼參數、電子郵件地址和密碼來判斷使用者是否可登入IPS。 如果使用者&#x200B;*可以*&#x200B;登入，此方法會傳回字串`ValidLogin`。 如果使用者&#x200B;*無法*&#x200B;登入，此方法會傳回字串`InvalidLogin`。

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
