---
description: 標準化大小。 用於指定影像大小或矩形大小，相對於圖層0或某些其它影像的大小進行歸一化。
solution: Experience Manager
title: 大小N
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 58c2d7da-31fc-49d1-a404-2e4a66ff0e56
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 0%

---

# 大小N{#sizen}

標準化大小。 用於指定影像大小或矩形大小，相對於圖層0或某些其它影像的大小進行歸一化。

<table id="simpletable_BB36205775D4447084E527E2630D28B9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 大小N</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>。 <span class="codeph"><span class="varname"> 無</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>。 <span class="codeph"><span class="varname"> 無</span></span> </p></td> 
  <td class="stentry"> <p>與另一影像（實數、實數、大於0）的歸一化寬度和高度 </p></td> 
 </tr> 
</table>

兩者 *nx* 和 *無* 必須大於0。 0,0可能表示應使用特定預設大小。 1,1指定與參考影像相等的大小。
