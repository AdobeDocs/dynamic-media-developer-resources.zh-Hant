---
title: 可重複的紋理
description: 可重複的紋理包括內部和外部材料，如織物（服裝和裝飾）、牆到壁的地板覆蓋物、牆紙、檯面材料、木紋紋理、屋面和壁面材料，以及任何其它普通紋理。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3693498b-994a-460a-8b2e-780a1482d37a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 3%

---

# 可重複的紋理{#repeatable-textures}

可重複的紋理包括內部和外部材料，如織物（服裝和裝飾）、牆到壁的地板覆蓋物、牆紙、檯面材料、木紋紋理、屋面和壁面材料，以及任何其它普通紋理。

可重複紋理可應用於平整、流線、草繪、平面、壁和機櫃對象。 當應用到非紋理對象時，將使用 `color=` 或 `bgc=` 如果 `color=` 未指定)。

如果材料包括 `src=` 屬性，指定影像，如果影像出現在除貼圖或壁邊框之外的MSS中。

渲染時，通過匹配 `anchor=` 紋理材料的點與對象的紋理原點（如在視頻中創作的）。

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>可重複紋理影像；要求 </p> </td> 
   <td colname="col3"> <p>無。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> 雷斯= </span> </a> </p> </td> 
   <td colname="col2"> <p>紋理解析度 </p> </td> 
   <td colname="col3"> <span class="codeph"> 屬性：：解析度 </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> 錨= </span> </a> </p> </td> 
   <td colname="col2"> <p>紋理對齊點 </p> </td> 
   <td colname="col3"> <p>左上角。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> 重複= </span> </a> </p> </td> 
   <td colname="col2"> <p>重複模式 </p> </td> 
   <td colname="col3"> <p>0（直重複）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> 急= </span> </a> </p> </td> 
   <td colname="col2"> <p>銳利化 </p> </td> 
   <td colname="col3"> <p>0（無銳化）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

除了這些基本屬性外，可重複紋理還支援高級應用程式的以下特殊用途屬性：

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a" type="reference" format="dita" scope="local"> <span class="codeph"> 灌漿= </span> </a> </p> </td> 
   <td colname="col2"> <p>灌漿顏色和厚度；用於陶瓷/石磚材料 </p> </td> 
   <td colname="col3"> <p>影像中已存在的灌漿 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7" type="reference" format="dita" scope="local"> <span class="codeph"> 對齊= </span> </a> </p> </td> 
   <td colname="col2"> <p>對齊模式（對象之間）;用於裝飾應用 </p> </td> 
   <td colname="col3"> <p>中心匹配 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rotate.md#reference-3745d74a913e4065b7ac009fb4fd9e3c" type="reference" format="dita" scope="local"> <span class="codeph"> rotate= </span> </a> </p> </td> 
   <td colname="col2"> <p>紋理旋轉角；不支援壁對象 </p> </td> 
   <td colname="col3"> <p>0（無旋轉） </p> </td> 
  </tr> 
 </tbody> 
</table>
