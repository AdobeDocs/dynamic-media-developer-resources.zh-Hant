---
description: 獲取特定欄位中使用的字元的清單。
solution: Experience Manager
title: getUserChars
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d6b79c06-0e90-406f-bac8-3b8c2bae5480
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 12%

---

# getUserChars{#getuserchars}

獲取特定欄位中使用的字元的清單。

語法

## 授權用戶類型 {#section-7023871be4d2442daf51ff060ca06d9a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-93107d87f1b24fc8ad276dfee5e30b63}

**輸入(getUserCharsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`char欄位`*` | `xsd:string` | 是 | 確定要搜索的垃圾狀態。 |
| `*`包括非活動`*` | `xsd:boolean` | 是 | 包括或排除非活動用戶。 非IPS管理員用戶必須是至少一家公司的活動成員，才能被授權進行任何API調用。 如果用戶沒有有效的公司成員資格，則返回授權錯誤。 |
| `*`包含無效`*` | `xsd:boolean` | 否 | 包括或排除無效用戶。 |
| `*`companyHandleArray`*` | `types:HandleArray` | 否 | 根據公司篩選結果。 |
| `*`groupHandleArray`*` | `types:HandleArray` | 否 | 根據組篩選結果。 |
| `*`userRoleArray`*` | `types:StringArray` | 否 | 根據用戶角色篩選結果。 |
| `*`數字字元`*` | `xsd:int` | 否 | 啟用>1個字元。 |

**輸出(getUserCharsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`userCharsArray`*` | `types:StringArray` | 是 | 字元前置詞的陣列。 |

## 範例 {#section-3702f165e8b041139a6144f4a76ca25f}

此代碼示例返回：

* 特定公司用戶姓氏的首個字元。
* 一組組。
* 一組用戶角色。

用戶字元篩選器欄位字串常數確定返回的用戶字元的類型。

**請求**

```java
<ns1:getUserCharsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:charField>LastName</ns1:charField>
   <ns1:includeInvalid>false</ns1:includeInvalid>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:getUserCharsParam>
```

**回答**

```java
<getUserCharsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userCharsArray>
      <items>b</items>
      <items>c</items>
      <items>d</items>
   </userCharsArray>
</getUserCharsReturn>
```
