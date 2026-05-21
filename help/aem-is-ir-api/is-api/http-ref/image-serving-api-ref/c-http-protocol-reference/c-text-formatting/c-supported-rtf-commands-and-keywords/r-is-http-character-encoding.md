---
title: 字元編碼
description: 請使用下列命令來編碼字元。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a03f08f7-e9cc-458f-9ff0-7721f1dbc4cc
TQID: 'https://experienceleague.adobe.com/rptRmm7xxUUF2l5WTYXjvbaifW2z5XKeCQIqa5XLFh4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 94
ht-degree: 2%

---

# 字元編碼{#character-encoding}

請使用下列命令來編碼字元。

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
   <td> <p>單一8位元字元。 </p> </td> 
   <td> <p><span class="varname"> HH</span>必須是2位數的十六進位值。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\u<span class="varname"> N</span></span> </td> 
   <td> <p>單一Unicode字元。 </p> </td> 
   <td> <p><span class="varname"> N</span>是有符號的2位元組整數，因此大於32767的Unicode值必須表示為負數。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\uc<span class="varname"> N</span></span> </td> 
   <td> <p>Unicode字元大小。 </p> </td> 
   <td> <p>與指定Unicode字元對應的位元組數。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \loch </span> </td> 
   <td> <p>低ANSI區域的字元。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \hich </span> </td> 
   <td> <p>高ANSI區域的字元。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \dbch </span> </td> 
   <td> <p>後面跟著雙位元組字元。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>
