---
description: 支援以下段落格式命令。
solution: Experience Manager
title: 段落格式
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a2235082-714c-4ae3-ae06-c91ea2fb5abb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '235'
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
   <td> <p>將段落格式重置為預設值。 </p> </td> 
   <td> <p> <span class="codeph"> textPs=僅 </span> 限 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ql  </span> </td> 
   <td> <p>左對齊文字。 </p> </td> 
   <td> <p>預設. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qr  </span> </td> 
   <td> <p>靠右對齊文字。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qc  </span> </td> 
   <td> <p>水準居中文字。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qj  </span> </td> 
   <td> <p>水準對齊文本。 </p> </td> 
   <td> <p> <span class="codeph"> textPs=僅 </span> 限 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastql  </span> </td> 
   <td> <p>左對齊段落的最後一行。 </p> </td> 
   <td> <p>預設；<span class="codeph"> textPs= </span>;若<span class="codeph"> \qj </span>未作用，則忽略。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqr  </span> </td> 
   <td> <p>對齊對齊段落的最後一行。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 僅；如果\ <span class="codeph"> qj未 </span> 激活，則忽略。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqc  </span> </td> 
   <td> <p>居中對齊段落的最後一行。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 僅；如果\ <span class="codeph"> qj未 </span>激活，則忽略。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqj  </span> </td> 
   <td> <p>對合理段落的最後一行進行加以限定（拉伸）。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 僅；如果\ <span class="codeph"> qj未 </span>激活，則忽略。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fi  <span class="varname"> N  </span> </span> </td> 
   <td> <p>首行縮進。 </p> </td> 
   <td> <p>扭曲；<span class="codeph"> textPs= </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \li  <span class="varname"> N  </span> </span> </td> 
   <td> <p>左縮進。 </p> </td> 
   <td> <p>扭曲；<span class="codeph"> textPs= </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ri  <span class="varname"> N  </span> </span> </td> 
   <td> <p>右縮進。 </p> </td> 
   <td> <p>扭曲；<span class="codeph"> textPs= </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sl  <span class="varname"> N  </span> </span> </td> 
   <td> <p>行之間的間距。 </p> </td> 
   <td> <p>0（預設值）用於自動行距；值為正值，當大於預設行距時，僅使用值；為負值以強制間距。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \slmult  <span class="varname"> N  </span> </span> </td> 
   <td> <p>行距多個標誌。 </p> </td> 
   <td> <p>如果<span class="codeph"> \sl </span>為twip，則設為0（預設值），如果<span class="codeph"> \sl </span>為預設間距的倍數，則設為1。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sb  <span class="varname"> N  </span> </span> </td> 
   <td> <p>段落前的額外空格。 </p> </td> 
   <td> <p>扭曲；<span class="codeph"> text= </span>將<span class="codeph"> \sb </span>應用於文本框中的第一段，<span class="codeph"> textPs= </span>則不適用。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sa  <span class="varname"> N  </span> </span> </td> 
   <td> <p>段落後的額外空格。 </p> </td> 
   <td> <p>扭曲；<span class="codeph"> text= </span>將<span class="codeph"> \sa </span>應用到文本框中的最後一段，<span class="codeph"> textPs= </span>則不適用。 </p> </td> 
  </tr> 
 </tbody> 
</table>
