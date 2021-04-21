---
description: 文本框支援以下文檔屬性。
solution: Experience Manager
title: 文檔（文本框）屬性
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 1%

---


# 文檔（文本框）屬性{#document-text-box-properties}

文本框支援以下文檔屬性。

<table id="table_8E1DF8E6BD894D7A9ACFC839918E2315"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>命令</b> </th> 
   <th class="entry"> <b>說明</b> </th> 
   <th class="entry"> <b>附註</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \fontbl  </span> </td> 
   <td> <p>字型表格。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fcharset  <span class="varname"> N  </span> </span> </td> 
   <td> <p>字型<i>N</i>的字元集。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \colorbl  </span> </td> 
   <td> <p>RGB色彩表。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cmykcolortbl  </span> </td> 
   <td> <p>CMYK色彩表。 </p> </td> 
   <td> <p>Dynamic Media分機。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \*\iscolortbl  </span> </td> 
   <td> <p>影像伺服顏色的色彩表。 </p> </td> 
   <td> <p>Dynamic Media分公司；<span class="codeph"> textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \red  <span class="varname"> N  </span> </span> </td> 
   <td> <p>紅色元件。 </p> </td> 
   <td> <p>只能出現在<span class="codeph"> \colortbl </span>;0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \green  <span class="varname"> N  </span> </span> </td> 
   <td> <p>綠色元件。 </p> </td> 
   <td> <p>只能出現在<span class="codeph"> \colortbl </span>;0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \blue  <span class="varname"> N  </span> </span> </td> 
   <td> <p>藍色元件。 </p> </td> 
   <td> <p>只能出現在<span class="codeph"> \colortbl </span>;0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cyan  <span class="varname"> N  </span> </span> </td> 
   <td> <p>青色顏色元件。 </p> </td> 
   <td> <p>Dynamic Media分公司；可能只出現在<span class="codeph"> \cmykcolortbl </span>中；0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \magenta  <span class="varname"> N  </span> </span> </td> 
   <td> <p>洋紅色元件。 </p> </td> 
   <td> <p>Dynamic Media分公司；可能只出現在<span class="codeph"> \cmykcolortbl </span>中；0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \yellow  <span class="varname"> N  </span> </span> </td> 
   <td> <p>黃色元件。 </p> </td> 
   <td> <p>Dynamic Media分公司；可能只出現在<span class="codeph"> \cmykcolortbl </span>中；0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \black  <span class="varname"> N  </span> </span> </td> 
   <td> <p>黑色元件。 </p> </td> 
   <td> <p>Dynamic Media分公司；可能只出現在<span class="codeph"> \cmykcolortbl </span>中；0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margl  <span class="varname"> N  </span> </span> </td> 
   <td> <p>左邊距。 </p> </td> 
   <td> <p>扭轉；<span class="codeph"> textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margr  <span class="varname"> N  </span> </span> </td> 
   <td> <p>利潤。 </p> </td> 
   <td> <p>扭轉；<span class="codeph"> textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margt  <span class="varname"> N  </span> </span> </td> 
   <td> <p>最高利潤。 </p> </td> 
   <td> <p>扭轉；<span class="codeph"> textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margb  <span class="varname"> N  </span> </span> </td> 
   <td> <p>底部邊界。 </p> </td> 
   <td> <p>扭轉；<span class="codeph"> textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalt  </span> </td> 
   <td> <p>文字方塊中的對齊上方文字。 </p> </td> 
   <td> <p>預設 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalb  </span> </td> 
   <td> <p>文字方塊中的底部對齊文字。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalc  </span> </td> 
   <td> <p>將文字置於文字方塊中。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \stextflow  <span class="varname"> N  </span> </span> </td> 
   <td> <p>文字流方向。 </p> </td> 
   <td> <p>特定語言的文字流程；<span class="codeph"> textPs= </span>僅0（預設值）左右、上下（歐洲）1上下、左右（遠東） </p> </td> 
  </tr> 
 </tbody> 
</table>

