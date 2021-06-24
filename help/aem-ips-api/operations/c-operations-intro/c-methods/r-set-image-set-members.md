---
description: 設定與影像集相關聯的資產清單。
solution: Experience Manager
title: setImageSetMembers
feature: Dynamic Media Classic, SDK/API，影像集
role: Developer,Administrator
exl-id: c30df5fe-e355-45d4-8c06-e396caca0d58
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 12%

---

# setImageSetMembers{#setimagesetmembers}

設定與影像集相關聯的資產清單。

此操作忽略`ImageSets`和`SpinSets`的`pageReset`參數，並強制將值設為true。

## 授權的使用者類型 {#section-8968d6a39a344cfc8521020d92ae8916}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用戶必須具有對映像集資產的讀寫訪問權，並具有對每個成員資產的讀訪問權。

## 參數 {#section-2f46efcd24c648aeacba738509426e46}

**Input(setImageSetMembersParam)**

<table id="table_0CBBB65BCEFD4125A4069A080DFC873A"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>公司負責人。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 影像集句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> memberArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：ImageSetMemberUpdateArray</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 屬於影像集的資產成員陣列。 </td> 
  </tr> 
 </tbody> 
</table>

**輸出(setImageSetMembersReturn)**

IPS API不會針對此操作傳回回應。

## 範例 {#section-7b87219034464aa98524178ccee27738}

此代碼示例使用成員陣列來設定影像集的成員。

**請求**

```java
<setImageSetMembersParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <assetHandle>34205|22|929</assetHandle>
   <memberArray>
      <items>
         <assetHandle>24266|1|17062</assetHandle>
         <pageReset>true</pageReset>
      </items>
   </memberArray>
</setImageSetMembersParam>
```

**回答**

無。
