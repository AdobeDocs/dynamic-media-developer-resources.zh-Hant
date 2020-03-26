---
description: 重設一或多個資產的發佈狀態，以強制在下一個發佈工作中重新發佈資產。
seo-description: 重設一或多個資產的發佈狀態，以強制在下一個發佈工作中重新發佈資產。
seo-title: forceRepublishAssets
solution: Experience Manager
title: forceRepublishAssets
topic: Scene7 Image Production System API
uuid: fd1f4ece-075c-40e3-868a-f27b9a4c3374
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# forceRepublishAssets{#forcerepublishassets}

重設一或多個資產的發佈狀態，以強制在下一個發佈工作中重新發佈資產。

語法

## 授權使用者類型 {#section-3d5a3e3afea748d69845de5c8c376448}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-fd3f4dde9e984240b6f3e6d7a8db4e78}

**輸入(forceRepublishAssetsParam)**

<table id="table_742D67AD77554904976EC4A07A0CBC64"> 
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
   <td colname="col1"> <span class="codeph"> 公 <span class="varname"> 司控制</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>對包含要重設資產的公司進行處理。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"> 重 <span class="varname"> 新發佈檔案</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>指定資產的檔案會重新發佈至傳送伺服器。 預設為 <span class="codeph"> true</span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"> <span class="varname"> 重新同步目錄</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>指定用於提供資產的目錄中繼資料會同步，以確保是最新的。 此參數用於解決同一記錄的近乎並行更新時可能發生的競爭條件。 Defaults to <span class="codeph"> false</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandleArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：HandleArray</span> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>要重設發佈狀態的資產的控制代碼陣列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**輸出(forceRepublishAssetsParam)**

<table id="table_78E74186669F477E9E2D837D58A789DC"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishStateUpdateArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：PublishStateUpdateArray</span> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>發佈狀態更新的陣列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

