---
description: 檢查具有特定公司（由句柄識別）、電子郵件地址和密碼的用戶是否可以登入。
seo-description: 檢查具有特定公司（由句柄識別）、電子郵件地址和密碼的用戶是否可以登入。
seo-title: checkLogin
solution: Experience Manager
title: checkLogin
topic: Scene7 Image Production System API
uuid: 69f9e5f6-50c2-403d-93b2-b84a01f512a9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# checkLogin{#checklogin}

檢查具有特定公司（由句柄識別）、電子郵件地址和密碼的用戶是否可以登入。

>[!NOTE]
>
>如果省略公司句柄，此方法會檢查預設使用者的登入。

## 授權使用者類型 {#section-df8b26b550854f899948276adaca083a}

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
| ` *`companyHandle`*` | `xsd:string` | 否 | 包含使用者之公司的控制代碼。 |
| ` *`電子郵件`*` | `xsd:string` | 是 | 使用者的電子郵件地址。 |
| ` *`密碼`*` | `xsd:string` | 是 | 用戶密碼。 |

**輸出(checkLoginParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`狀態`*` | `xsd:string` | 是 | 使用者登入狀態。 |

## 範例 {#section-23f90100a9d94bc7b4045634cccd1b98}

此范常式式碼使用公司控制代碼參數、電子郵件地址和密碼來判斷使用者是否可登入IPS。 如果用戶 *可以登* 錄，此方法將返回字串 `ValidLogin`。 如果用戶 *無法登* 入，此方法會傳回字串 `InvalidLogin`。

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

