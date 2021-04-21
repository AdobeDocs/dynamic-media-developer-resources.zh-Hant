---
description: 傳回公司控制代碼所指定之公司的使用者。
solution: Experience Manager
title: getCompanyMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 16%

---


# getCompanyMembers{#getcompanymembers}

傳回公司控制代碼所指定之公司的使用者。

語法

## 授權用戶類型{#section-b2bc2fa0cc944cea8be82524838307cc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-5602e4d6f2214e398e6a804e61f1a088}

**輸入(getCompanyMembersParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 您要取得其成員的公司的控制代碼。 |
| `*`includeInvalid`*` | `xsd:boolean` | 是 | 包含無效的公司。 |

**輸出(getCompanyMembersReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`memberArray`*` | `types:CompanyMemberArray` | 是 | 使用者會籍的陣列。 |

## 範例 {#section-39d8cf3653fd4fe8b842caabac9dedfc}

此程式碼範例會傳回使用者陣列中公司的所有成員。 回應已因簡短而截斷。

**請求**

```java
<ns1:getCompanyMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:includeInvalid>false</ns1:includeInvalid>
</ns1:getCompanyMembersParam>
```

**回答**

```java
<getCompanyMembersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <memberArray>
      <items>
         <userHandle>66|pbayol@adobe.com</userHandle>
         <firstName>Peter</firstName>
         <lastName>Bayol</lastName>
         <email>pbayol@adobe.com</email>
         <role>IpsAdmin</role>
         <isValid>true</isValid>
         <passwordExpires>2107-07-25T23:12:49.472-07:00</passwordExpires>
      </items>
      ...
   </memberArray>
</getCompanyMembersReturn>
```

