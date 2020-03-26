---
description: 運行特定作業。
seo-description: 運行特定作業。
seo-title: executeJob
solution: Experience Manager
title: executeJob
topic: Scene7 Image Production System API
uuid: e73223c1-9032-4745-92b6-a5840949a824
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# executeJob{#executejob}

運行特定作業。

語法

## 授權使用者類型 {#section-8199e8599ea64e7097a2acb633417b15}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-2c61b2bffcf9479a9391f2c13fdf7d53}

**輸入(executeJobParam)**

<table id="table_FA410513908F4084A21A5F0A9431006C"> 
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
   <td colname="col1"> <p><span class="codeph"> 公 <span class="varname"> 司控制</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>工作所屬公司的控制代碼。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> jobHandle</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>要運行的作業的句柄。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**輸出(executeJobReturn)**

IPS API不會傳回此作業的回應。

## 範例 {#section-96f71aa58a954293b9a98ff96d86f232}

此程式碼範例會執行排程在IPS中執行的工作。

**請求**

```java
<executeJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</executeJobParam>
```

**回答**

無。
