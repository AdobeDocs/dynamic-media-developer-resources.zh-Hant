---
description: 獲取由公司、組和用戶角色句柄指定的一組用戶。 此操作可讓您依字元排序傳回的使用者及篩選。
solution: Experience Manager
title: getUsers
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 10%

---


# getUsers{#getusers}

獲取由公司、組和用戶角色句柄指定的一組用戶。 此操作可讓您依字元排序傳回的使用者及篩選。

## 授權用戶類型{#section-6a8f23cc6b22442d8776f701016971ed}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`


| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`includeInactive`*` | `xsd:boolean` | 否 | 包含或排除非作用中使用者。 非IPS管理員使用者必須是至少一家公司的有效成員，才能取得進行任何API呼叫的授權。 如果使用者沒有有效的公司會籍，則會傳回授權錯誤。 |
| `*`includeInvalid`*` | `xsd:boolean` | 否 | 可讓您包含／排除無效使用者。 |
| `*`companyHandleArray`*` | `types:HandleArray` | 否 | 依公司篩選結果。 |
| `*`groupHandleArray`*` | `types:HandleArray` | 否 | 依群組篩選結果。 |
| `*`userRoleArray`*` | `types:StringArray` | 否 | 依使用者角色篩選結果。 |
| `*`charFilterField`*` | `xsd:string` | 否 | 依欄位字串首碼篩選結果(請參閱[!DNL Trash State).] |
| `*`charFilter`*` | `xsd:string` | 否 | 依特定字元篩選結果。 |
| `*`sortBy`*` | `xsd:string` | 否 | 用戶排序欄位的選擇。 |
| `*`recordsPerPage`*` | `xsd:int` | 否 | 傳回每頁指定的記錄數。 |
| `*`resultsPage`*` | `xsd:int` | 否 | 結果頁面。 |

**輸出(getUsersReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`userArray`*` | `types:UserArray` | 是 | 一組使用者。 |

## 範例 {#section-bc43a5dd7b4c4f048d25fc881554dab2}

此程式碼範例會傳回數個選用參數的使用者陣列。 用戶角色、用戶字元過濾器欄位和用戶排序欄位是通過使用特定字串常數來確定的。

**請求**

```java
<ns1:getUsersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:includeInvalid>false</ns1:includeInvalid>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
   <ns1:userRoleArray>
      <ns1:items>IpsAdmin</ns1:items>
   </ns1:userRoleArray>
   <ns1:sortBy>LastName</ns1:sortBy>
</ns1:getUsersParam>
```

**回答**

```java
<getUsersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userArray>
      <items>
         <userHandle>70|kmagnusson@adobe.com</userHandle>
         <firstName>Kris</firstName>
         <lastName>Magnusson</lastName>
         <email>kmagnusson@adobe.com</email>
         <role>IpsAdmin</role>
         <isValid>true</isValid>
         <passwordExpires>2107-07-27T15:18:15.816-07:00</passwordExpires>
      </items>
      ...
   </userArray>
</getUsersReturn>
```

