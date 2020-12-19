---
description: 當在壁邊界MSS中指定材料時，該材料被視為壁邊界（以sub=3..5引入）。
seo-description: 當在壁邊界MSS中指定材料時，該材料被視為壁邊界（以sub=3..5引入）。
seo-title: 牆邊界
solution: Experience Manager
title: 牆邊界
topic: Scene7 Image Serving - Image Rendering API
uuid: 40acd667-5e8b-4425-b44a-0681e608d189
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# 壁邊框{#wall-borders}

當在壁邊界MSS中指定材料時，該材料被視為壁邊界（以sub=3..5引入）。

壁邊框紋理影像可以包括α通道以定義邊框的形狀。 壁邊框只能應用於壁對象。

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src=  </span> </a> </p> </td> 
   <td colname="col2"> <p>可重複的紋理影像；必要 </p> </td> 
   <td colname="col3"> <p>無 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res=  </span> </a> </p> </td> 
   <td colname="col2"> <p>紋理解析度 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> 屬性：：解析度  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> 錨點=  </span> </a> </p> </td> 
   <td colname="col2"> <p>水準紋理對齊（忽略y值） </p> </td> 
   <td colname="col3"> <p>0（左側影像邊緣） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp=  </span> </a> </p> </td> 
   <td colname="col2"> <p>銳利化 </p> </td> 
   <td colname="col3"> <p>0（無銳利化） </p> </td> 
  </tr> 
 </tbody> 
</table>

