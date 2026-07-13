---
title: removeFolderPermissions
description: 移除檔案夾許可權。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 10830980-d504-4610-96c9-730937453256
TQID: 'https://experienceleague.adobe.com/HrnWyUVLEVifP87zhZiJF6BXMCZdqLFO3Q1adxH71RI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 102
ht-degree: 10%

---

# removeFolderPermissions{#removefolderpermissions}

移除檔案夾許可權。

語法

## 授權的使用者型別 {#section-bfa745624f9b43aaba6c226ac6700fe7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-7efa68377fd846219b906d354ae64ed3}

**輸入(removeFolderPermissionsParam)**

<table id="table_15223256C63C4F008BDB1DF6F0AFE6A8"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 具有您要移除之檔案夾許可權的公司控制代碼。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 資料夾的控制代碼。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> updateChildren</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：布林值</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> <p>當<span class="codeph"> true</span>時： 
     <ul id="ul_1305D060E0F34A61AA3C827E43F296E6"> 
      <li id="li_AB8705F3CEAD4B8A8F1C28291A6F7EC8">許可權移除會傳播到所有檔案夾許可權作業。 </li> 
     </ul> </p> <p>當<span class="codeph"> false</span>時： 
     <ul id="ul_19AEE80F1FC84B64AD623E050C12A0CD"> 
      <li id="li_B8B78851004C43DB8CB7958E380AF510">此操作只會影響指定的資料夾。 </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**輸出(removeFolderPermissionsReturn)**

IPS API未傳回此作業的回應。

## 範例 {#section-04390f0ec7cc460cb5d34d518e33e7a5}

此程式碼範例從檔案夾及其子檔案夾中移除許可權。 將`updateChildren`設為`false`僅從父資料夾中移除許可權。

**要求**

```java
<removeFolderPermissionsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>64</companyHandle>
   <folderHandle>blackmesa/Awatermark/</folderHandle>
   <updateChildren>true</updateChildren>
</removeFolderPermissionsParam>
```

**回應**

無。

