---
description: 支援下列段落格式命令。
solution: Experience Manager
title: 段落格式
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a2235082-714c-4ae3-ae06-c91ea2fb5abb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# 段落格式{#paragraph-formatting}

支援下列段落格式命令。

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
   <td> <p> 僅<span class="codeph"> textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ql </span> </td> 
   <td> <p>文字靠左對齊。 </p> </td> 
   <td> <p>預設。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qr </span> </td> 
   <td> <p>文字靠右對齊。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qc </span> </td> 
   <td> <p>將文字水準置中。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qj </span> </td> 
   <td> <p>水準對齊文字。 </p> </td> 
   <td> <p> 僅<span class="codeph"> textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastql </span> </td> 
   <td> <p>靠左對齊段落的最後一行。 </p> </td> 
   <td> <p>預設；僅限<span class="codeph"> textPs= </span>；如果<span class="codeph"> \qj </span>未啟用，則會略過。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqr </span> </td> 
   <td> <p>以右對齊對齊段落的最後一行。 </p> </td> 
   <td> <p> 僅<span class="codeph"> textPs= </span>；如果<span class="codeph"> \qj </span>未啟用，則會略過。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqc </span> </td> 
   <td> <p>將齊行段落的最後一行置中。 </p> </td> 
   <td> <p> 僅<span class="codeph"> textPs= </span>；如果<span class="codeph"> \qj </span>未啟用，則會略過。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqj </span> </td> 
   <td> <p>將（延伸）對齊段落的最後一行。 </p> </td> 
   <td> <p> 僅<span class="codeph"> textPs= </span>；如果<span class="codeph"> \qj </span>未啟用，則會略過。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fi <span class="varname"> N </span> </span> </td> 
   <td> <p>第一行縮排。 </p> </td> 
   <td> <p>Twips；僅<span class="codeph"> textPs= </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \li <span class="varname"> N </span> </span> </td> 
   <td> <p>左邊縮排。 </p> </td> 
   <td> <p>Twips；僅<span class="codeph"> textPs= </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ri <span class="varname"> N </span> </span> </td> 
   <td> <p>右邊縮排。 </p> </td> 
   <td> <p>Twips；僅<span class="codeph"> textPs= </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sl <span class="varname"> N </span> </span> </td> 
   <td> <p>行間距。 </p> </td> 
   <td> <p>0 （預設）表示自動行距；正值表示僅在大於預設行距時使用值；負值表示強制行距。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \slmult <span class="varname"> N </span> </span> </td> 
   <td> <p>行距多重旗標。 </p> </td> 
   <td> <p>如果<span class="codeph"> \sl </span>是以twips表示，則設為0 （預設）；如果<span class="codeph"> \sl </span>是預設間距的倍數，則設為1。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sb <span class="varname"> N </span> </span> </td> 
   <td> <p>段落前額外空格。 </p> </td> 
   <td> <p>Twips； <span class="codeph"> text= </span>將<span class="codeph"> \sb </span>套用至文字方塊中的第一個段落，<span class="codeph"> textPs= </span>沒有。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sa <span class="varname"> N </span> </span> </td> 
   <td> <p>段落後額外空格。 </p> </td> 
   <td> <p>Twips； <span class="codeph"> text= </span>將<span class="codeph"> \sa </span>套用至文字方塊中的最後一個段落，<span class="codeph"> textPs= </span>沒有。 </p> </td> 
  </tr> 
 </tbody> 
</table>
