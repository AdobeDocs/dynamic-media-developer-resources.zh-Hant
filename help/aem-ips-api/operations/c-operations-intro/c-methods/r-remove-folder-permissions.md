---
description: 移除檔案夾權限。
solution: Experience Manager
title: removeFolderPermissions
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 16%

---


# removeFolderPermissions{#removefolderpermissions}

移除檔案夾權限。

語法

## 授權用戶類型{#section-bfa745624f9b43aaba6c226ac6700fe7}

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
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 具有您要移除之權限之資料夾的公司控制代碼。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 資料夾的句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> updateChildren</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> <p>當<span class="codeph"> true</span>: 
     <ul id="ul_1305D060E0F34A61AA3C827E43F296E6"> 
      <li id="li_AB8705F3CEAD4B8A8F1C28291A6F7EC8">權限刪除會通過所有資料夾權限操作傳播。 </li> 
     </ul> </p> <p>當<span class="codeph"> false</span>: 
     <ul id="ul_19AEE80F1FC84B64AD623E050C12A0CD"> 
      <li id="li_B8B78851004C43DB8CB7958E380AF510">此操作僅影響指定的資料夾。 </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**輸出(removeFolderPermissionsReturn)**

IPS API不會傳回此作業的回應。

## 範例 {#section-04390f0ec7cc460cb5d34d518e33e7a5}

此程式碼範例會移除資料夾及其子資料夾的權限。 如果只需要從父資料夾中刪除權限，請將`updateChildren`設定為`false`。

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
