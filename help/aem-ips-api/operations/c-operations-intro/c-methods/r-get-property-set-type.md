---
description: 使用公司句柄和屬性集類型的名稱獲取屬性集類型。 它將獲取一個類型結構，其中該類型的句柄以及屬性類型。
solution: Experience Manager
title: getPropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ff9c3d24-577c-4a9c-8820-60c2a33773bc
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 11%

---

# getPropertySetType{#getpropertysettype}

使用公司句柄和屬性集類型的名稱獲取屬性集類型。 它將獲取一個類型結構，其中該類型的句柄以及屬性類型。

語法

## 授權用戶類型 {#section-2b291d32f95b4a3d854429124cbae24c}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-c9a53400c44744668bd7915f72d2bf3d}

**Input(getPropertySetTypeParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 否 | 公司的把手。 可選，因為屬性集類型可以屬於多個公司。 |
| 名稱 | `xsd:string` | 是 | 屬性集類型名稱。 |

**輸出(getPropertySetTypeReturn)**

<table id="table_F2724F6B706C4F658AED99290E29F3E6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名稱 </th> 
   <th colname="col2" class="entry"> 類型 </th> 
   <th colname="col3" class="entry"> 必要 </th> 
   <th colname="col4" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 類型</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：PropertySetType</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4">包含以下項的類型結構： 
    <ul id="ul_FC028882124D4CD6870A076CBFB80333"> 
     <li id="li_9F36539C51ED48EDBECCD6A07A4FDD4A">把手。 </li> 
     <li id="li_6004406A0D1341648A714FF3C61E4004">鍵入名稱。 </li> 
     <li id="li_29F6CA9D8B134ED3B10B6BDBB41BF607">屬性類型。 </li> 
     <li id="li_A2354354541A4F1AB7234F65F2B61A40">指示類型是否允許多個屬性類型的值。 </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## 範例 {#section-1b57199415e34a8fa449f864f8895b14}

此代碼示例按名稱返回屬性集類型。

**請求**

```java
<getPropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <name>Adobe.UserProperty</name>
</getPropertySetTypeParam>
```

**回答**

```java
<getPropertySetTypeReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <type>
      <typeHandle>pt|10801</typeHandle>
      <name>Adobe.UserProperty</name>
      <propertyType>UserProperty</propertyType>
      <allowMultiple>false</allowMultiple></type>
</getPropertySetTypeReturn>
```
