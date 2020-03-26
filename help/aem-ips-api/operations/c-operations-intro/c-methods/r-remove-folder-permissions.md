---
description: 移除檔案夾權限。
seo-description: 移除檔案夾權限。
seo-title: removeFolderPermissions
solution: Experience Manager
title: removeFolderPermissions
topic: Scene7 Image Production System API
uuid: cd9f7a42-e314-4ec9-abe2-a27581c7cd23
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# removeFolderPermissions{#removefolderpermissions}

移除檔案夾權限。

語法

## 授權使用者類型 {#section-bfa745624f9b43aaba6c226ac6700fe7}

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
   <td colname="col1"> <span class="codeph"> 公 <span class="varname"> 司控制</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 具有您要移除之權限之資料夾的公司控制代碼。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> folderHandle <span class="varname"> (資料夾句柄</span> ) </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 資料夾的句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 更 <span class="varname"> 新子項</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> <p>若為 <span class="codeph"> 真</span>: 
     <ul id="ul_1305D060E0F34A61AA3C827E43F296E6"> 
      <li id="li_AB8705F3CEAD4B8A8F1C28291A6F7EC8">權限刪除會通過所有資料夾權限操作傳播。 </li> 
     </ul> </p> <p>若為 <span class="codeph"> false</span>: 
     <ul id="ul_19AEE80F1FC84B64AD623E050C12A0CD"> 
      <li id="li_B8B78851004C43DB8CB7958E380AF510">此操作僅影響指定的資料夾。 </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**輸出(removeFolderPermissionsReturn)**

IPS API不會傳回此作業的回應。

## 範例 {#section-04390f0ec7cc460cb5d34d518e33e7a5}

此程式碼範例會移除資料夾及其子資料夾的權限。 如果 `updateChildren` 您只 `false` 需要從父資料夾中移除權限，請設定為。

**請求**

```java
<removeFolderPermissionsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>64</companyHandle>
   <folderHandle>blackmesa/Awatermark/</folderHandle>
   <updateChildren>true</updateChildren>
</removeFolderPermissionsParam>
```

**回答**

無。
