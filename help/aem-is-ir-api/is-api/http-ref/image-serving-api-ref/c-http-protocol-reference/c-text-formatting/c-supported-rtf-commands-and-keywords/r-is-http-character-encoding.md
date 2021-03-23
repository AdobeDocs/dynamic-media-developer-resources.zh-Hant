---
description: 使用下列命令來編碼字元。
seo-description: 使用下列命令來編碼字元。
seo-title: 字元編碼
solution: Experience Manager
title: 字元編碼
uuid: 7b19b831-b40c-4f26-83a4-732c578dbbf0
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 1%

---


# 字元編碼{#character-encoding}

使用下列命令來編碼字元。

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
   <td> <p><span class="varname"> </span> hh必須是2位十六進位值。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\<span class="varname"> uN</span></span> </td> 
   <td> <p>單一Unicode字元。 </p> </td> 
   <td> <p><span class="varname"> </span> Nis a signed 2 byter and a so a Unicode value thas the 32767 must be experated a number. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\<span class="varname"> ucN</span></span> </td> 
   <td> <p>Unicode字元大小。 </p> </td> 
   <td> <p>與給定Unicode字元對應的位元組數。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \loch  </span> </td> 
   <td> <p>下面是低ANSI區域的字元。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \hick  </span> </td> 
   <td> <p>高ANSI區域的字元如下。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \dbch  </span> </td> 
   <td> <p>接著是雙位元組字元。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

