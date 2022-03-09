---
title: 資產作業日誌
description: 與特定資產關聯的作業日誌條目的詳細資訊。 getAssetJobLogs返回的資料。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 2c8ebec2-a664-46cd-b843-9893bfa0a9d1
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 16%

---

# 資產作業日誌{#assetjoblog}

與特定資產關聯的作業日誌條目的詳細資訊。 getAssetJobLogs返回的資料。

語法

## 參數 {#section-5da4d6156b7f4ca88a67202fbf736104}

<table id="table_7BC785BC95EA43D582D1B2289FF3130D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名稱 </th> 
   <th colname="col2" class="entry"> 類型 </th> 
   <th colname="col3" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 作業句柄</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 作業處理。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 作業名稱</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：字串</span> </td> 
   <td colname="col3"> 工作名稱. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 日誌消息</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：字串</span> </td> 
   <td colname="col3">作業日誌中的消息。 <p><span class="codeph"> 日誌消息</span> 響應欄位基於 <span class="codeph"> auth標頭</span> 區域設定欄位。 </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 日誌類型</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：字串</span> </td> 
   <td colname="col3"> 日誌條目中的作業類型。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 提交用戶電子郵件</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：字串</span> </td> 
   <td colname="col3"> 提交作業的用戶的電子郵件。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 日誌日期</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 作業日期。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> aux陣列</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：JobLogDetailArray</span> </td> 
   <td colname="col3"> 每個作業日誌的輔助作業日誌消息陣列。 </td> 
  </tr> 
 </tbody> 
</table>
