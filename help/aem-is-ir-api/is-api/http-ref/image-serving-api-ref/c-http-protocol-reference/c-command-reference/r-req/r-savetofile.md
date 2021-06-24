---
description: 將影像儲存至檔案。
solution: Experience Manager
title: saveToFile
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 10a8ea5c-7e64-4d99-a263-779f08ea6e37
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 3%

---

# saveToFile{#savetofile}

將影像儲存至檔案。

`req=saveToFile&name= *``*[&timeout= *`fileval`*]`

<table id="simpletable_5674FD9655FE4CDDB0E5DC8655890A66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> file</span> </p> </td> 
  <td class="stentry"> <p>目標影像檔案的相對路徑。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>逾時間隔（毫秒）。 </p></td> 
 </tr> 
</table>

將響應映像保存到伺服器上的檔案，而不是將其返回到客戶端。

儲存請求成功完成時，請求會傳回數個Java格式化屬性，其中包括：

<table id="table_8BA8F75A0B7241BAB9B4359F97C21137"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 屬性</b> </th> 
   <th class="entry"> <b> 類型</b> </th> 
   <th class="entry"> <b> 說明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> lastUpdated</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p>檔案建立時間（自1970年1月1日午夜以來的毫秒數）。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> pixelsTotal</span> </p> </td> 
   <td> <p> 整數 </p> </td> 
   <td> <p> 儲存影像中的像素數。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 狀態</span> </p> </td> 
   <td> <p> 列舉 </p> </td> 
   <td> <p> <span class="codeph"> </span> doneif成功。 </p> </td> 
  </tr> 
 </tbody> 
</table>

如果成功，則傳回HTTP回應狀態200；如果請求失敗或逾時，則傳回403。 回應的MIME類型`text/plain`且無法快取。

重要資訊：必須通過指定`attribute::SavePath`中現有可寫資料夾的路徑來啟用保存到檔案。 `saveToFile=` 如果為空 `attribute::SavePath` 則失敗。

*`file`* 為必要路徑，且必須是與結合的相對路 `attribute::SavePath`徑。影像伺服不會建立資料夾。 目標資料夾必須存在於伺服器上，並且具有適當的權限設定，以便「影像伺服」建立檔案。

`timeout=` 為選用。預設逾時為60,000毫秒，或以`PS::SaveTimeout`設定的值為準。
