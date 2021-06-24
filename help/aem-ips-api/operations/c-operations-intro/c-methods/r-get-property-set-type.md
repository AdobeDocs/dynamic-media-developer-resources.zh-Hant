---
description: 使用公司句柄獲取屬性集類型以及屬性集類型的名稱。 它將獲得一個類型結構，該類型具有對類型的句柄以及屬性類型。
solution: Experience Manager
title: getPropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: ff9c3d24-577c-4a9c-8820-60c2a33773bc
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 10%

---

# getPropertySetType{#getpropertysettype}

使用公司句柄獲取屬性集類型以及屬性集類型的名稱。 它將獲得一個類型結構，該類型具有對類型的句柄以及屬性類型。

語法

## 授權的使用者類型 {#section-2b291d32f95b4a3d854429124cbae24c}

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

**輸入(getPropertySetTypeParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 否 | 公司的把手。 選用，因為屬性集類型可屬於多個公司。 |
| `*`名稱`*` | `xsd:string` | 是 | 屬性集類型名稱。 |

**Output(getPropertySetTypeReturn)**

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> type</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:PropertySetType</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4">包含的類型結構： 
    <ul id="ul_FC028882124D4CD6870A076CBFB80333"> 
     <li id="li_9F36539C51ED48EDBECCD6A07A4FDD4A">控制。 </li> 
     <li id="li_6004406A0D1341648A714FF3C61E4004">類型名稱。 </li> 
     <li id="li_29F6CA9D8B134ED3B10B6BDBB41BF607">屬性類型。 </li> 
     <li id="li_A2354354541A4F1AB7234F65F2B61A40">指示類型是否允許多個屬性類型的值。 </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## 範例 {#section-1b57199415e34a8fa449f864f8895b14}

此程式碼範例會依名稱傳回屬性集類型。

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
