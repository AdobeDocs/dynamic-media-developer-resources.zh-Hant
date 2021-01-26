---
description: 標準化大小。 用於指定影像大小或矩形大小，並相對於圖層0或其他影像的大小進行標準化。
seo-description: 標準化大小。 用於指定影像大小或矩形大小，並相對於圖層0或其他影像的大小進行標準化。
seo-title: sizeN
solution: Experience Manager
title: sizeN
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 6fc05654-6f0d-499f-97bc-6b7134024e1f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---


# sizeN{#sizen}

標準化大小。 用於指定影像大小或矩形大小，並相對於圖層0或其他影像的大小進行標準化。

<table id="simpletable_BB36205775D4447084E527E2630D28B9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>標準化寬度和高度（實際、實際、大於0） </p></td> 
 </tr> 
</table>

*nx*&#x200B;和&#x200B;*ny*&#x200B;都必須大於0。 0,0可能表示應使用特定的預設大小。 1,1指定與參考影像相等的大小。
