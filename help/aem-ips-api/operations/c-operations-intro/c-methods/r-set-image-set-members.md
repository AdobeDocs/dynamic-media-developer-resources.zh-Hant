---
description: 設定與影像集關聯的資產清單。
seo-description: 設定與影像集關聯的資產清單。
seo-title: setImageSetMembers
solution: Experience Manager
title: setImageSetMembers
topic: Scene7 Image Production System API
uuid: 84a73ff4-e93f-4764-80e8-e15f1fec1aeb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setImageSetMembers{#setimagesetmembers}

設定與影像集關聯的資產清單。

此操作會忽略 `pageReset` 和的 `ImageSets` 參數 `SpinSets` ，並強制將值設定為true。

## 授權使用者類型 {#section-8968d6a39a344cfc8521020d92ae8916}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用戶必須擁有映像集資產的讀和寫訪問權限，並且必須擁有對每個成員資產的讀訪問權限。

## 參數 {#section-2f46efcd24c648aeacba738509426e46}

**輸入(setImageSetMembersParam)**

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
   <td colname="col1"> <p><span class="codeph"> 公 <span class="varname"> 司控制</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>公司負責人。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 資 <span class="varname"> 產控制代碼</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 影像集控點。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> memberArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：ImageSetMemberUpdateArray</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 屬於映像集的資產成員陣列。 </td> 
  </tr> 
 </tbody> 
</table>

**輸出(setImageSetMembersReturn)**

IPS API不會傳回此作業的回應。

## 範例 {#section-7b87219034464aa98524178ccee27738}

此代碼示例使用成員陣列來設定映像集的成員。

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
