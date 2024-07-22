---
description: 將影像儲存至檔案。
solution: Experience Manager
title: saveToFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 10a8ea5c-7e64-4d99-a263-779f08ea6e37
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 1%

---

# saveToFile{#savetofile}

將影像儲存至檔案。

`req=saveToFile&name= *`檔案`*[&timeout= *`值`*]`

<table id="simpletable_5674FD9655FE4CDDB0E5DC8655890A66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">檔案</span> </p> </td> 
  <td class="stentry"> <p>目標影像檔案的相對路徑。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">值</span> </p></td> 
  <td class="stentry"> <p>逾時間隔（毫秒）。 </p></td> 
 </tr> 
</table>

將回應影像儲存至伺服器上的檔案，而非傳回給使用者端。

儲存請求成功完成時，該請求會傳回數個Java格式屬性，包括下列內容：

<table id="table_8BA8F75A0B7241BAB9B4359F97C21137"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>屬性</b> </th> 
   <th class="entry"> <b>型別</b> </th> 
   <th class="entry"> <b>描述</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph">上次更新時間</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p>檔案建立時間（自午夜以來的毫秒數，1970 UTC/GMT 1月1日）。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph">畫素總計</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> 已儲存影像中的畫素數。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph">狀態</span> </p> </td> 
   <td> <p> 列舉 </p> </td> 
   <td> <p> 如果成功，<span class="codeph">完成</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

如果成功，則傳回HTTP回應狀態200；如果請求失敗或逾時，則傳回403。 回應具有MIME型別`text/plain`，無法快取。

重要您必須指定`attribute::SavePath`中現有可寫入資料夾的路徑，以啟用儲存至檔案。 如果`attribute::SavePath`是空的，`saveToFile=`會失敗。

*`file`*&#x200B;為必要項，且必須是與`attribute::SavePath`結合的相對路徑。 「影像伺服」不會建立資料夾。 目標資料夾必須存在於伺服器上，且具備適當的許可權設定，可供「影像伺服」建立檔案。

`timeout=`是選用專案。 預設逾時為60,000毫秒，或是以`PS::SaveTimeout`設定的任一值。
