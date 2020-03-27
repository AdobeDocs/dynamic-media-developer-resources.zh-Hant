---
description: 支援以下段落格式命令。
seo-description: 支援以下段落格式命令。
seo-title: 段落格式
solution: Experience Manager
title: 段落格式
topic: Scene7 Image Serving - Image Rendering API
uuid: 4f9255b2-3a74-4c9a-80c5-d85b4627027e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 段落格式{#paragraph-formatting}

支援以下段落格式命令。

<table id="table_5DD044E1C0614A29A2413557DF57197D"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>命令 </p> </th> 
   <th class="entry"> <p>說明 </p> </th> 
   <th class="entry"> <p>附註 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \pard </span> </td> 
   <td> <p>將段落格式重設為預設值。 </p> </td> 
   <td> <p> <span class="codeph"> textPs=僅 </span> 限 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ql </span> </td> 
   <td> <p>左對齊文字。 </p> </td> 
   <td> <p>預設. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qr </span> </td> 
   <td> <p>右對齊文字。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qc </span> </td> 
   <td> <p>水準置中文字。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qj </span> </td> 
   <td> <p>水準對齊文字。 </p> </td> 
   <td> <p> <span class="codeph"> textPs=僅 </span> 限 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastql </span> </td> 
   <td> <p>左對齊段落的最後一行。 </p> </td> 
   <td> <p>預設值；僅 <span class="codeph"> 限textPs= </span> ;如果 <span class="codeph"> \qj未 </span>激活，則忽略。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqr </span> </td> 
   <td> <p>右對齊合法段落的最後一行。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only;如果 <span class="codeph"> \qj未 </span> 激活，則忽略。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqc </span> </td> 
   <td> <p>將正當段落的最後一行置中。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only;如果 <span class="codeph"> \qj未 </span>激活，則忽略。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqj </span> </td> 
   <td> <p>對合理段落的最後一行加以限定（延伸）。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only;如果 <span class="codeph"> \qj未 </span>激活，則忽略。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fi <span class="varname"> N </span></span> </td> 
   <td> <p>首行縮進。 </p> </td> 
   <td> <p>扭轉； <span class="codeph"> textPs=僅 </span> 限。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \li <span class="varname"> N </span></span> </td> 
   <td> <p>左縮進。 </p> </td> 
   <td> <p>扭轉； <span class="codeph"> textPs=僅 </span> 限。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ri <span class="varname"> n </span></span> </td> 
   <td> <p>右縮進。 </p> </td> 
   <td> <p>扭轉； <span class="codeph"> textPs=僅 </span> 限。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sl <span class="varname"> n </span></span> </td> 
   <td> <p>行之間的間距。 </p> </td> 
   <td> <p>0（預設值）用於自動行距；正值僅用於大於預設行距時的值；為負值以強制間距。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \slmult <span class="varname"> n </span></span> </td> 
   <td> <p>行間距多個標誌。 </p> </td> 
   <td> <p>如果\sl為twips，則設 <span class="codeph"> 置為0( </span> 預設值)，如果 <span class="codeph"></span> \sl為預設間距的倍數，則設定為1。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sb <span class="varname"> N </span></span> </td> 
   <td> <p>段落前加上空格。 </p> </td> 
   <td> <p>扭轉； <span class="codeph"> text= </span>會套用 <span class="codeph"> \sb </span> 至文字方塊中的第一個段落， <span class="codeph"> textPs= </span> 則否。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sa <span class="varname"> N </span></span> </td> 
   <td> <p>段落後面有額外的空間。 </p> </td> 
   <td> <p>扭轉； <span class="codeph"> text= </span> 應用 <span class="codeph"> \sa </span> 到文本框中的最後一個段落， <span class="codeph"> textPs= </span> 則否。 </p> </td> 
  </tr> 
 </tbody> 
</table>

