---
description: 獲取由公司、組和用戶角色句柄指定的用戶陣列。 此操作允許您按字元對返回的用戶進行排序和篩選。
solution: Experience Manager
title: getUsers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dfdcbcdd-232f-4c73-9520-c7c958eedf54
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 10%

---

# getUsers{#getusers}

獲取由公司、組和用戶角色句柄指定的用戶陣列。 此操作允許您按字元對返回的用戶進行排序和篩選。

## 授權用戶類型 {#section-6a8f23cc6b22442d8776f701016971ed}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`


| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 包括非活動 | `xsd:boolean` | 否 | 包括或排除非活動用戶。 非IPS管理員用戶必須是至少一家公司的活動成員，才能被授權進行任何API調用。 如果用戶沒有有效的公司成員資格，則返回授權錯誤。 |
| includeInvalid | `xsd:boolean` | 否 | 允許您包括/排除無效用戶。 |
| companyHandleArray | `types:HandleArray` | 否 | 按公司篩選結果。 |
| groupHandleArray | `types:HandleArray` | 否 | 按組篩選結果。 |
| userRoleArray | `types:StringArray` | 否 | 按用戶角色篩選結果。 |
| charFilterField | `xsd:string` | 否 | 按欄位的字串前置詞篩選結果(請參見 [!DNL Trash State).] |
| char篩選器 | `xsd:string` | 否 | 按特定字元篩選結果。 |
| 排序依據 | `xsd:string` | 否 | 用戶排序欄位的選擇。 |
| 記錄每頁 | `xsd:int` | 否 | 返回每頁指定的記錄數。 |
| 結果頁 | `xsd:int` | 否 | 結果頁面。 |

**輸出(getUsersReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 用戶陣列 | `types:UserArray` | 是 | 一組用戶。 |

## 範例 {#section-bc43a5dd7b4c4f048d25fc881554dab2}

此代碼示例返回多個可選參數的用戶陣列。 用戶角色、用戶字元篩選器欄位和用戶排序欄位是使用特定字串常數確定的。

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
