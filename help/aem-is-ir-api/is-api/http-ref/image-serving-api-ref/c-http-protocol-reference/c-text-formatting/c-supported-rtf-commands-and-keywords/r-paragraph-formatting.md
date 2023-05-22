---
description: 支援以下段落格式命令。
solution: Experience Manager
title: 段落格式
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a2235082-714c-4ae3-ae06-c91ea2fb5abb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '230'
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
   <td> <span class="codeph"> \pard </span> </td> 
   <td> <p>將段落格式重置為預設值。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 僅 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ql </span> </td> 
   <td> <p>左對齊文本。 </p> </td> 
   <td> <p>預設. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qr </span> </td> 
   <td> <p>右對齊文本。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qc </span> </td> 
   <td> <p>水準居中文本。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qj </span> </td> 
   <td> <p>水準對齊文本。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 僅 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastql </span> </td> 
   <td> <p>左對齊段落的最後一行。 </p> </td> 
   <td> <p>預設； <span class="codeph"> textPs= </span> 僅；忽略 <span class="codeph"> \qj </span>不活動。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqr </span> </td> 
   <td> <p>右對齊正文段落的最後一行。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 僅；忽略 <span class="codeph"> \qj </span> 不活動。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastq </span> </td> 
   <td> <p>將正文段落的最後一行居中。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 僅；忽略 <span class="codeph"> \qj </span>不活動。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqj </span> </td> 
   <td> <p>對正確段落的最後一行進行定義（拉伸）。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 僅；忽略 <span class="codeph"> \qj </span>不活動。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fi <span class="varname"> N </span> </span> </td> 
   <td> <p>首行縮進。 </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> 只是。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \li <span class="varname"> N </span> </span> </td> 
   <td> <p>左縮進。 </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> 只是。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ri <span class="varname"> N </span> </span> </td> 
   <td> <p>右縮進。 </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> 只是。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sl <span class="varname"> N </span> </span> </td> 
   <td> <p>行間間距。 </p> </td> 
   <td> <p>0（預設值）用於自動行距；正值，僅當大於預設行距時使用值；為負值以強制間距。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \slmult <span class="varname"> N </span> </span> </td> 
   <td> <p>行間距多標誌。 </p> </td> 
   <td> <p>如果設定為0（預設） <span class="codeph"> \sl </span> 為twips，如果為1 <span class="codeph"> \sl </span> 為預設間距的倍數。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sb <span class="varname"> N </span> </span> </td> 
   <td> <p>段落前的額外空格。 </p> </td> 
   <td> <p>Twips; <span class="codeph"> 文本= </span>應用 <span class="codeph"> \sb </span> 到文本框中的第一段， <span class="codeph"> textPs= </span> 不會。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sa <span class="varname"> N </span> </span> </td> 
   <td> <p>段落後的額外空間。 </p> </td> 
   <td> <p>Twips; <span class="codeph"> 文本= </span> 應用 <span class="codeph"> \sa </span> 文本框的最後一段， <span class="codeph"> textPs= </span> 不會。 </p> </td> 
  </tr> 
 </tbody> 
</table>
