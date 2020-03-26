---
description: 與特定資產相關聯的作業日誌條目的詳細資訊。 getAssetJobLogs傳回的資料。
seo-description: 與特定資產相關聯的作業日誌條目的詳細資訊。 getAssetJobLogs傳回的資料。
seo-title: AssetJobLog
solution: Experience Manager
title: AssetJobLog
topic: Scene7 Image Production System API
uuid: 0dd65da1-f358-4d9a-98a2-abfb036347e3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# AssetJobLog{#assetjoblog}

與特定資產相關聯的作業日誌條目的詳細資訊。 getAssetJobLogs傳回的資料。

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 工作代理。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobName</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 工作名稱. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> logMessage</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">作業日誌中的消息。 <p><span class="codeph"> logMessage</span> response欄位會根據authHeader地區 <span class="codeph"> 設定欄位進行本地化</span> 。 </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> logType</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 日誌條目中的作業類型。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> submitUserEmail</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 提交工作的使用者電子郵件。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> logDate</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 工作日期。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> auxArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：JobLogDetailArray</span> </td> 
   <td colname="col3"> 每個作業日誌的輔助作業日誌消息陣列。 </td> 
  </tr> 
 </tbody> 
</table>

