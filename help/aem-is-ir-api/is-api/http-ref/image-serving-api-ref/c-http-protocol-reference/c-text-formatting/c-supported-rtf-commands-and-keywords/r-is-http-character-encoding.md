---
description: 對字元進行編碼時，請使用下列命令。
solution: Experience Manager
title: 字元編碼
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: a03f08f7-e9cc-458f-9ff0-7721f1dbc4cc
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 2%

---

# 字元編碼{#character-encoding}

對字元進行編碼時，請使用下列命令。

<table id="table_EB0C1B674BEA4A37964FB4BF559E0005"> 
 <thead> 
  <tr> 
   <th class="entry"> 命令 </th> 
   <th class="entry"> 說明 </th> 
   <th class="entry"> 附註 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph">\'<span class="varname"> HH</span></span> </td> 
   <td> <p>單一8位字元。 </p> </td> 
   <td> <p><span class="varname"> </span> 必須是2位十六進位值。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\<span class="varname"> uN</span></span> </td> 
   <td> <p>單一Unicode字元。 </p> </td> 
   <td> <p><span class="varname"> </span> Nis為帶符號的2個位元組整數，因此大於32767的Unicode值必須表示為負數。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\<span class="varname"> ucN</span></span> </td> 
   <td> <p>Unicode字元大小。 </p> </td> 
   <td> <p>與給定Unicode字元對應的位元組數。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \loch  </span> </td> 
   <td> <p>低ANSI區域的字元後跟。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \hic  </span> </td> 
   <td> <p>高ANSI區域的字元後面跟著。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \dbch  </span> </td> 
   <td> <p>後面接著雙位元組字元。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>
