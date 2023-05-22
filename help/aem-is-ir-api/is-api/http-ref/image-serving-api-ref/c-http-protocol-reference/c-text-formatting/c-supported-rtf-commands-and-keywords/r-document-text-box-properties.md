---
description: 文本框支援以下文檔屬性。
solution: Experience Manager
title: 文檔（文本框）屬性
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e9d21a39-4d98-4115-8179-ab5acf713c80
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '209'
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
   <td> <span class="codeph"> \fontbl </span> </td> 
   <td> <p>字型表。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fcharset <span class="varname"> N </span> </span> </td> 
   <td> <p>字型字元集 <i>N</i>。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \colorbl </span> </td> 
   <td> <p>RGB顏色表。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cmykcolorbl </span> </td> 
   <td> <p>CMYK顏色表。 </p> </td> 
   <td> <p>Dynamic Media分機。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \*\iscolorbl </span> </td> 
   <td> <p>「影像服務」顏色的顏色表。 </p> </td> 
   <td> <p>Dynamic Media延期； <span class="codeph"> textPs= </span> 僅 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \紅色 <span class="varname"> N </span> </span> </td> 
   <td> <p>紅色元件。 </p> </td> 
   <td> <p>可能只出現在 <span class="codeph"> \colorbl </span>;0..255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \綠色 <span class="varname"> N </span> </span> </td> 
   <td> <p>綠色元件。 </p> </td> 
   <td> <p>可能只出現在 <span class="codeph"> \colorbl </span>;0..255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \藍色 <span class="varname"> N </span> </span> </td> 
   <td> <p>藍色元件。 </p> </td> 
   <td> <p>可能只出現在 <span class="codeph"> \colorbl </span>;0..255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \青色 <span class="varname"> N </span> </span> </td> 
   <td> <p>青色元件。 </p> </td> 
   <td> <p>Dynamic Media延期；只能顯示 <span class="codeph"> \cmykcolorbl </span>;0..100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \洋紅色 <span class="varname"> N </span> </span> </td> 
   <td> <p>洋紅色分量。 </p> </td> 
   <td> <p>Dynamic Media延期；只能顯示 <span class="codeph"> \cmykcolorbl </span>;0..100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> 黃色 <span class="varname"> N </span> </span> </td> 
   <td> <p>黃色元件。 </p> </td> 
   <td> <p>Dynamic Media延期；只能顯示 <span class="codeph"> \cmykcolorbl </span>;0..100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> 黑 <span class="varname"> N </span> </span> </td> 
   <td> <p>黑色元件。 </p> </td> 
   <td> <p>Dynamic Media延期；只能顯示 <span class="codeph"> \cmykcolorbl </span>;0..100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margl <span class="varname"> N </span> </span> </td> 
   <td> <p>左邊距。 </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> 僅 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margr <span class="varname"> N </span> </span> </td> 
   <td> <p>右邊距。 </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> 僅 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \marg <span class="varname"> N </span> </span> </td> 
   <td> <p>上邊距。 </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> 僅 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margb <span class="varname"> N </span> </span> </td> 
   <td> <p>底邊距。 </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> 僅 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertal </span> </td> 
   <td> <p>文本框中的頂對齊文本。 </p> </td> 
   <td> <p>預設 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertall </span> </td> 
   <td> <p>文本框中的下對齊文本。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertal </span> </td> 
   <td> <p>將文本居中在文本框中。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \stextflow <span class="varname"> N </span> </span> </td> 
   <td> <p>文本流方向。 </p> </td> 
   <td> <p>特定語言的文本流； <span class="codeph"> textPs= </span> 僅0（預設）左右，上下（歐洲）1上下，左右（遠東） </p> </td> 
  </tr> 
 </tbody> 
</table>
