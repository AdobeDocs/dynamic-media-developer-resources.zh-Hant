---
description: 支援以下段落格式命令。
solution: Experience Manager
title: 段落格式
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 1%

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
   <td> <span class="codeph"> \pard  </span> </td> 
   <td> <p>將段落格式重設為預設值。 </p> </td> 
   <td> <p> <span class="codeph"> textPs=僅 </span> 限 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ql  </span> </td> 
   <td> <p>左對齊文字。 </p> </td> 
   <td> <p>預設. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qr  </span> </td> 
   <td> <p>右對齊文字。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qc  </span> </td> 
   <td> <p>水準置中文字。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qj  </span> </td> 
   <td> <p>水準對齊文字。 </p> </td> 
   <td> <p> <span class="codeph"> textPs=僅 </span> 限 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastql  </span> </td> 
   <td> <p>左對齊段落的最後一行。 </p> </td> 
   <td> <p>預設值；<span class="codeph"> textPs= </span>;如果<span class="codeph"> \qj </span>未作用，則忽略。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqr  </span> </td> 
   <td> <p>右對齊合法段落的最後一行。 </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only;如果 <span class="codeph"> \qj未 </span> 激活，則忽略。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqc  </span> </td> 
   <td> <p>將正當段落的最後一行置中。 </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only;如果 <span class="codeph"> \qj未 </span>激活，則忽略。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqj  </span> </td> 
   <td> <p>對合理段落的最後一行加以限定（延伸）。 </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only;如果 <span class="codeph"> \qj未 </span>激活，則忽略。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fi  <span class="varname"> N  </span> </span> </td> 
   <td> <p>首行縮進。 </p> </td> 
   <td> <p>扭轉；<span class="codeph"> textPs= </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \li  <span class="varname"> N  </span> </span> </td> 
   <td> <p>左縮進。 </p> </td> 
   <td> <p>扭轉；<span class="codeph"> textPs= </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ri  <span class="varname"> N  </span> </span> </td> 
   <td> <p>右縮進。 </p> </td> 
   <td> <p>扭轉；<span class="codeph"> textPs= </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sl  <span class="varname"> N  </span> </span> </td> 
   <td> <p>行之間的間距。 </p> </td> 
   <td> <p>0（預設值）用於自動行距；正值僅用於大於預設行距時的值；為負值以強制間距。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \slmult  <span class="varname"> n  </span> </span> </td> 
   <td> <p>行間距多個標誌。 </p> </td> 
   <td> <p>如果<span class="codeph"> \sl </span>為twips，則設定為0（預設）；如果<span class="codeph"> \sl </span>為預設間距的倍數，則設定為1。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sb  <span class="varname"> N  </span> </span> </td> 
   <td> <p>段落前加上空格。 </p> </td> 
   <td> <p>扭轉；<span class="codeph"> text= </span>將<span class="codeph"> \sb </span>套用至文字方塊中的第一段，<span class="codeph"> textPs= </span>則否。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sa  <span class="varname"> N  </span> </span> </td> 
   <td> <p>段落後面有額外的空間。 </p> </td> 
   <td> <p>扭轉；<span class="codeph"> text= </span>將<span class="codeph"> \sa </span>套用至文字方塊中的最後一段，<span class="codeph"> textPs= </span>則否。 </p> </td> 
  </tr> 
 </tbody> 
</table>

