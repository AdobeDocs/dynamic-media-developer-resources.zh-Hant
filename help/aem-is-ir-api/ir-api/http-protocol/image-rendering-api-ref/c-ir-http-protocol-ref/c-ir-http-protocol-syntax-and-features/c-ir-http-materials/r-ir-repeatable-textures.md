---
description: 可重複的紋理包括內部和外部材料，例如織物（包括服裝和內飾）、牆對壁地板覆蓋物、牆紙、檯面材料、木紋紋理、屋面和壁板材料，以及任何其他普通紋理。
solution: Experience Manager
title: 可重複的紋理
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 3%

---


# 可重複的紋理{#repeatable-textures}

可重複的紋理包括內部和外部材料，例如織物（包括服裝和內飾）、牆對壁地板覆蓋物、牆紙、檯面材料、木紋紋理、屋面和壁板材料，以及任何其他普通紋理。

可重複的紋理可套用至平面、流線、素描、平面、壁和機櫃物件。 當套用至非文字物件時，物件會上色為`color=`（若未指定`color=`，則為`bgc=`）。

如果材料包含指定影像的`src=`屬性，並且該屬性發生在非貼圖或壁邊框的MSS中，則該材料被視為紋理。

在渲染時，通過匹配紋理材料的`anchor=`點與對象的紋理原點（如在暈映中創作），紋理與對象對齊。

<table id="table_992A6E93E4274B598A236F8F728F017A"> 
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
   <td colname="col3"> <p>無。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res=  </span> </a> </p> </td> 
   <td colname="col2"> <p>紋理解析度 </p> </td> 
   <td colname="col3"> <span class="codeph"> 屬性：：解析度  </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> 錨點=  </span> </a> </p> </td> 
   <td colname="col2"> <p>紋理對齊點 </p> </td> 
   <td colname="col3"> <p>左上角。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> 重複=  </span> </a> </p> </td> 
   <td colname="col2"> <p>重複模式 </p> </td> 
   <td colname="col3"> <p>0（直重複）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp=  </span> </a> </p> </td> 
   <td colname="col2"> <p>銳利化 </p> </td> 
   <td colname="col3"> <p>0（無銳利化）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

除了這些基本屬性外，可重複的紋理還支援下列進階應用程式的特殊用途屬性：

<table id="table_A97365804CB143DEB31F26A65DA3CE04"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
   <th colname="col3" class="entry"> <p>預設 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a" type="reference" format="dita" scope="local"> <span class="codeph"> 灌漿=  </span> </a> </p> </td> 
   <td colname="col2"> <p>灌漿的顏色和厚度；用於陶瓷／石磚材料 </p> </td> 
   <td colname="col3"> <p>影像中已存在的漿料 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7" type="reference" format="dita" scope="local"> <span class="codeph"> align=  </span> </a> </p> </td> 
   <td colname="col2"> <p>對齊模式（對象之間）;用於裝飾應用 </p> </td> 
   <td colname="col3"> <p>中間匹配 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rotate.md#reference-3745d74a913e4065b7ac009fb4fd9e3c" type="reference" format="dita" scope="local"> <span class="codeph"> rotate= </span> </a> </p> </td> 
   <td colname="col2"> <p>紋理旋轉角度；不支援牆體物件 </p> </td> 
   <td colname="col3"> <p>0（無旋轉） </p> </td> 
  </tr> 
 </tbody> 
</table>

