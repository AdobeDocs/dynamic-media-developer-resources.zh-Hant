---
description: 文本框支援以下文檔屬性。
solution: Experience Manager
title: 文檔（文本框）屬性
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: e9d21a39-4d98-4115-8179-ab5acf713c80
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '214'
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
   <td> <p>字型表。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fcharset  <span class="varname"> N  </span> </span> </td> 
   <td> <p>字型<i>N</i>的字元集。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \colorbl  </span> </td> 
   <td> <p>RGB顏色表。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cmykcolortbl  </span> </td> 
   <td> <p>CMYK顏色表。 </p> </td> 
   <td> <p>Dynamic Media擴充功能。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \*\iscolortbl  </span> </td> 
   <td> <p>影像提供顏色的顏色表。 </p> </td> 
   <td> <p>Dynamic Media擴充功能；<span class="codeph"> textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \red  <span class="varname"> N  </span> </span> </td> 
   <td> <p>紅色元件。 </p> </td> 
   <td> <p>只能出現在<span class="codeph"> \colortbl </span>中；0..255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \green  <span class="varname"> N  </span> </span> </td> 
   <td> <p>綠色元件。 </p> </td> 
   <td> <p>只能出現在<span class="codeph"> \colortbl </span>中；0..255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \blue  <span class="varname"> N  </span> </span> </td> 
   <td> <p>藍色元件。 </p> </td> 
   <td> <p>只能出現在<span class="codeph"> \colortbl </span>中；0..255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \青色 <span class="varname"> N  </span> </span> </td> 
   <td> <p>青色顏色元件。 </p> </td> 
   <td> <p>Dynamic Media擴充功能；只能出現在<span class="codeph"> \cmykcolortbl </span>中；0..100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \magenta  <span class="varname"> N  </span> </span> </td> 
   <td> <p>洋紅色分量。 </p> </td> 
   <td> <p>Dynamic Media擴充功能；只能出現在<span class="codeph"> \cmykcolortbl </span>中；0..100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \黃色 <span class="varname"> N  </span> </span> </td> 
   <td> <p>黃色元件。 </p> </td> 
   <td> <p>Dynamic Media擴充功能；只能出現在<span class="codeph"> \cmykcolortbl </span>中；0..100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \black  <span class="varname"> N  </span> </span> </td> 
   <td> <p>黑色元件。 </p> </td> 
   <td> <p>Dynamic Media擴充功能；只能出現在<span class="codeph"> \cmykcolortbl </span>中；0..100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margl  <span class="varname"> N  </span> </span> </td> 
   <td> <p>左邊距。 </p> </td> 
   <td> <p>扭曲；<span class="codeph"> textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margr  <span class="varname"> N  </span> </span> </td> 
   <td> <p>右邊。 </p> </td> 
   <td> <p>扭曲；<span class="codeph"> textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margt  <span class="varname"> N  </span> </span> </td> 
   <td> <p>最大利潤。 </p> </td> 
   <td> <p>扭曲；<span class="codeph"> textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margb  <span class="varname"> N  </span> </span> </td> 
   <td> <p>下邊距。 </p> </td> 
   <td> <p>扭曲；<span class="codeph"> textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalt  </span> </td> 
   <td> <p>文字方塊中的靠上對齊文字。 </p> </td> 
   <td> <p>預設 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalb  </span> </td> 
   <td> <p>文本框中的靠下對齊文本。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalc  </span> </td> 
   <td> <p>在文本框中居中文本。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \stextflow  <span class="varname"> N  </span> </span> </td> 
   <td> <p>文字流方向。 </p> </td> 
   <td> <p>特定語言的文本流；<span class="codeph"> textPs= </span>僅0（預設值）左右、上下（歐洲）1上下、右左（遠東） </p> </td> 
  </tr> 
 </tbody> 
</table>
