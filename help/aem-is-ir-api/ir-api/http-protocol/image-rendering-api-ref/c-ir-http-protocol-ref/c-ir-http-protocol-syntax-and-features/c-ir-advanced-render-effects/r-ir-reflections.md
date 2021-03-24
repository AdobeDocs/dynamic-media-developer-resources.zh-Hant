---
description: 您可編寫暈映，以包含近3D反射資料。
solution: Experience Manager
title: 反射
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 3%

---


# 反射{#reflections}

您可編寫暈映，以包含近3D反射資料。

如果創作了該屬性，則使用以下材料屬性定義材料的反射表面屬性：

<table id="table_8769C726A17E412FB41F7CB87690B1FE"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>屬性 </p> </th> 
   <th class="entry"> <p>說明 </p> </th> 
   <th class="entry"> <p>預設 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca" type="reference" format="dita" scope="local"> <span class="codeph"> 光澤=</span> </a> </p> </td> 
   <td> <p>表面光澤度 </p> </td> 
   <td> <p>從暈映 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a" type="reference" format="dita" scope="local"> <span class="codeph"> glosmap=  </span> </a> </p> </td> 
   <td> <p>光澤變化（灰階影像） </p> </td> 
   <td> <p>無 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180" type="reference" format="dita" scope="local"> <span class="codeph"> 粗糙=  </span> </a> </p> </td> 
   <td> <p>表面粗糙度 </p> </td> 
   <td> <p>40% </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35" type="reference" format="dita" scope="local"> <span class="codeph"> type=</span> </a> </p> </td> 
   <td> <p>材料類型 </p> </td> 
   <td> <p>0（未知） </p> </td> 
  </tr> 
 </tbody> 
</table>

渲染器根據`type=`調整`gloss=`和`rough=`屬性的範圍。 某些材料類型如織物通常比諸如石頭或金屬等材料類型反射更少，並且為一種材料指定的相同光澤量將導致與另一種材料不同的反射效果。 `gloss=`未指定或設為0時，粗 `type=` 糙度具有相當寬的色域。

`glossmap=` 可用於逐個像素控制材料的光澤度。
