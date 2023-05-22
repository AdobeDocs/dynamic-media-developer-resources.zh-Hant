---
description: 將影像保存到檔案。
solution: Experience Manager
title: 保存到檔案
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 10a8ea5c-7e64-4d99-a263-779f08ea6e37
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 3%

---

# 保存到檔案{#savetofile}

將影像保存到檔案。

`req=saveToFile&name= *`檔案`*[&timeout= *`谷`*]`

<table id="simpletable_5674FD9655FE4CDDB0E5DC8655890A66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> file</span> </p> </td> 
  <td class="stentry"> <p>目標影像檔案的相對路徑。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 谷</span> </p></td> 
  <td class="stentry"> <p>超時間隔（毫秒）。 </p></td> 
 </tr> 
</table>

將響應映像保存到伺服器上的檔案，而不是將其返回到客戶端。

成功完成保存請求後，請求將返回幾個Java格式的屬性，包括：

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
   <td> <p> <span class="codeph"> 上次更新</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p>檔案建立時間（自1970年1月1日午夜以來的毫秒數）。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 像素合計</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> 保存影像中的像素數。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 狀態</span> </p> </td> 
   <td> <p> 枚舉 </p> </td> 
   <td> <p> <span class="codeph"> 完成</span> 成功。 </p> </td> 
  </tr> 
 </tbody> 
</table>

如果成功，則返回HTTP響應狀態200；如果請求失敗或超時，則返回403。 響應具有MIME類型 `text/plain` 無法快取。

重要資訊：必須通過在中指定現有可寫資料夾的路徑來啟用保存到檔案 `attribute::SavePath`。 `saveToFile=` 失敗 `attribute::SavePath` 為空。

*`file`* 是必需的，且必須是與 `attribute::SavePath`。 映像服務不建立資料夾。 目標資料夾必須存在於伺服器上，並且具有映像服務建立檔案的相應權限設定。

`timeout=` 為可選項。 預設超時為60,000毫秒，或配置的值 `PS::SaveTimeout`。
