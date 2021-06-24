---
description: 獲取特定欄位中使用的字元的清單。
solution: Experience Manager
title: getUserChars
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: d6b79c06-0e90-406f-bac8-3b8c2bae5480
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 11%

---

# getUserChars{#getuserchars}

獲取特定欄位中使用的字元的清單。

語法

## 授權的使用者類型 {#section-7023871be4d2442daf51ff060ca06d9a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-93107d87f1b24fc8ad276dfee5e30b63}

**輸入(getUserCharsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`charField`*` | `xsd:string` | 是 | 決定要搜尋的垃圾桶狀態。 |
| `*`includeInactive`*` | `xsd:boolean` | 是 | 包含或排除非作用中使用者。 非IPS管理員使用者必須是至少一間公司的有效成員，才能獲得授權以進行任何API呼叫。 如果用戶沒有有效的公司成員資格，則將返回授權錯誤。 |
| `*`includeInvalid`*` | `xsd:boolean` | 否 | 包括或排除無效用戶。 |
| `*`companyHandleArray`*` | `types:HandleArray` | 否 | 根據公司篩選結果。 |
| `*`groupHandleArray`*` | `types:HandleArray` | 否 | 根據群組篩選結果。 |
| `*`userRoleArray`*` | `types:StringArray` | 否 | 根據使用者角色篩選結果。 |
| `*`numChars`*` | `xsd:int` | 否 | 啟用>1個字元。 |

**輸出(getUserCharsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`userCharsArray`*` | `types:StringArray` | 是 | 字元前置詞的陣列。 |

## 範例 {#section-3702f165e8b041139a6144f4a76ca25f}

此程式碼範例會傳回：

* 特定公司使用者姓氏的首字元。
* 一組群組。
* 一組使用者角色。

使用者字元篩選欄位字串常數決定傳回的使用者字元類型。

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
