---
description: 獲取有關用戶的資訊。 使用系統用戶的電子郵件地址和密碼作為授權請求的憑據。 否則，該操作將獲取有關預設用戶的資訊。
solution: Experience Manager
title: getUserInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1981f25f-779e-4434-ab6b-0debb40521fe
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 12%

---

# getUserInfo{#getuserinfo}

獲取有關用戶的資訊。 使用系統用戶的電子郵件地址和密碼作為授權請求的憑據。 否則，該操作將獲取有關預設用戶的資訊。

語法

## 授權用戶類型 {#section-1c42d78e914a4b84a946b3480f29b36a}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-e87b3cb743494719925c9458eed433b6}

**輸入(getUserInfoParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| userHandle | `xsd:string` | 否 | 處理要返回其資訊的用戶。 |
| 電子郵件 | `xsd:string` | 否 | 用戶電子郵件地址。 |

**輸出(getUserInfoReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 用戶資訊 | `types:User` | 是 | 用戶的名、姓、電子郵件地址和角色，以及用戶是否有效以及用戶密碼何時過期。 |

## 範例 {#section-98d77a2e360a438dbe240099bea26a65}

此代碼示例返回預設IPS用戶的資訊。

**請求**

```java
<getUserInfoParam xmlns="http://www.scene7.com/IpsApi/xsd" /></getUserInfoParam>
```

**回答**

```java
<ns1:getUserInfoReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd"> 
   <ns1:userInfo> 
      <ns1:userHandle>3261|user@scene7.com</ns1:userHandle> 
      <ns1:firstName>FirstName</ns1:firstName> 
      <ns1:lastName>LastName</ns1:lastName> 
      <ns1:email>user@scene7.com</ns1:email> 
      <ns1:role>IpsAdmin</ns1:role> 
      <ns1:isValid>true</ns1:isValid> 
      <ns1:passwordExpires>2107-04-22T18:35:41.995Z</ns1:passwordExpires> 
   </ns1:userInfo> 
</ns1:getUserInfoReturn>
```
