---
title: 牆邊界
description: 當材料在壁邊界MSS中指定時，它被視為壁邊界（帶子=3..5）。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e11c38d0-8255-4363-ae60-f47be37a1495
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 5%

---

# 牆邊界{#wall-borders}

當材料在壁邊界MSS中指定時，它被視為壁邊界（帶子=3..5）。

壁邊界紋理影像可以包括用於定義邊界形狀的α通道。 壁邊框只能應用於壁對象。

<table id="table_906C5CC4CADF4024AA0E29544AF48080"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
   <th colname="col3" class="entry"> <p>預設 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>可重複紋理影像；要求 </p> </td> 
   <td colname="col3"> <p>無 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> 雷斯= </span> </a> </p> </td> 
   <td colname="col2"> <p>紋理解析度 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> 屬性：：解析度 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> 錨= </span> </a> </p> </td> 
   <td colname="col2"> <p>水準紋理對齊（忽略y值） </p> </td> 
   <td colname="col3"> <p>0（左影像邊緣） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> 急= </span> </a> </p> </td> 
   <td colname="col2"> <p>銳利化 </p> </td> 
   <td colname="col3"> <p>0（無銳化） </p> </td> 
  </tr> 
 </tbody> 
</table>
