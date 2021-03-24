---
description: 取得使用者的相關資訊。 使用系統使用者的電子郵件地址和密碼作為授權請求的憑證。 否則，操作將獲取有關預設用戶的資訊。
solution: Experience Manager
title: getUserInfo
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 11%

---


# getUserInfo{#getuserinfo}

取得使用者的相關資訊。 使用系統使用者的電子郵件地址和密碼作為授權請求的憑證。 否則，操作將獲取有關預設用戶的資訊。

語法

## 授權用戶類型{#section-1c42d78e914a4b84a946b3480f29b36a}

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
| `*`userHandle`*` | `xsd:string` | 否 | 處理您要傳回其資訊的使用者。 |
| `*`電子郵件`*` | `xsd:string` | 否 | 使用者電子郵件地址。 |

**輸出(getUserInfoReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`userInfo`*` | `types:User` | 是 | 使用者的名字、姓氏、電子郵件地址和角色，以及使用者是否有效以及密碼過期。 |

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

