---
description: 將特定用戶或預設用戶的密碼設定為特定值（取決於您是否指定了用戶句柄）。
solution: Experience Manager
title: setPassword
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: e8d95b55-0a97-4887-b711-7be99833c389
source-git-commit: a05fb31b7c7515492723af63914d3e9999e65e9b
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 7%

---

# setPassword{#setpassword}

將特定用戶或預設用戶的密碼設定為特定值（取決於您是否指定了用戶句柄）。

密碼過期日期為可選。 如果省略，密碼就不會過期。

## 授權用戶類型 {#section-39ae61d78cab4492a6efc1fc0d2f06c4}

>[!NOTE]
>
>** 只有用 `IpsAdmin` 戶類型有權對其他用戶運行setPassword呼叫。

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`

## 參數 {#section-0531294341f7483d89dacaa393dd659a}

**輸入(setPasswordParam)**

<table id="table_BF54512811344E0B979C5070354E8048"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>名稱 </p> </th> 
   <th colname="col2" class="entry"> <p>類型 </p> </th> 
   <th colname="col3" class="entry"> <p>必要 </p> </th> 
   <th colname="col4" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> userHandle  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>用戶句柄。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 密碼  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string  </span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>密碼. </p> <p>對所選密碼強制執行下列要求： </p> <p> 
     <ul id="ul_E5BE3621127C476788412174584075B3"> 
      <li id="li_0132852AFD774659A0224C450F19418C">密碼區分大小寫。 </li> 
      <li id="li_71224B3A89C8461AB689BAD383EC8CEA">最小密碼長度為8個字元。 </li> 
      <li id="li_C21B6843EA734D1ABE0580185F775408">密碼必須包含以下字元類中的一個或多個字元： 
       <ul id="ul_D5D3911AD6214035BBD2AB8350A459C7"> 
        <li id="li_6E3F084100104F2CBCF130EF8852C7B7">小寫英文字元。 例如<span class="codeph"> a b c d e </span>等 </li> 
        <li id="li_1FDED8D7348842BC857320D797D41217">大寫英文字元。 例如， <span class="codeph"> A B C D E </span>等。 </li> 
        <li id="li_C3C4D5412AA749F3B78F37B2B696CF80">數量. 例如， <span class="codeph"> 1 2 3 4 5 </span>等。 </li> 
        <li id="li_2730798F26E74B878BEDE510CD06D8DD">特殊符號字元。 例如，您可以使用下列任一項：<span class="codeph"> &amp;grave;~ !@ # $ % ^ *(_ + - = { }) | [ ] &amp; \ :" ;「 &lt; &gt; ?, / </span> </li> 
       </ul> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> passwordExpires  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:dateTime  </span> </p> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>確定密碼的過期日期。 <p>注意： 為時區提供此欄位的要求。 時區會調整為中央時間。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

**輸出(setPasswordReturn)**

IPS API不會針對此操作傳回回應。

## 範例 {#section-23a6fbabdb3c4c3180076057e47ae567}

此程式碼範例會建立使用者密碼。 由於`passwordExpires`被忽略，密碼從未過期。

**請求**

```java
<ns1:setPasswordParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">  
   <ns1:userHandle>3341|juser@scene7.com</ns1:userHandle> 
   <ns1:password>@Do6e$ySt3mz</ns1:password> 
</ns1:setPasswordParam>
```

**回答**

無。
