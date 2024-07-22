---
title: 貼花
description: 貼花材料包括服裝結構，例如套衫、T恤印刷，以及刺繡或印刷的標誌。 它也包括用於內部或外部應用程式的不可重複平坦物件，例如區域地毯、掛牆藝術和標誌。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 07190abd-9f6f-46b5-bf77-cd97c48fc9be
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 1%

---

# 貼花{#decals}

貼花材料包括服裝結構，例如套衫、T恤印刷，以及刺繡或印刷的標誌。 它也包括用於內部或外部應用程式的不可重複平坦物件，例如區域地毯、掛牆藝術和標誌。

如果在貼花MSS中指定了材料，則將其視為貼花。 貼花通常是RGBA影像，Alpha色版定義貼花的形狀。

一個貼花可套用到每個平面、流程圖、草繪、平面或壁物件（除非已設定「無紋理」旗標）。 貼花會套用至物件，方法是將貼花的`anchor=`與暈映物件的貼花原點對齊。 可以使用`pos=`進一步調整位置。

如果貼花材料定義厚度，而暈映物件定義光向量，則會演算陰影。

<table id="table_3F119BC9B7654FD092826A34F5827268"> 
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
   <td colname="col2"> <p>影像（通常使用Alpha）；必要。 </p> </td> 
   <td colname="col3"> <p>無。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988" type="reference" format="dita" scope="local"> <span class="codeph">大小= </span> </a> </p> </td> 
   <td colname="col2"> <p>貼花寬度、高度和厚度（用於投影）。 </p> </td> 
   <td colname="col3"> <p> <span class="varname"> imageWidth </span> x <span class="codeph">解析度</span>，<span class="varname"> imageHeight </span> x <span class="codeph">解析度，0 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph">資源= </span> </a> </p> </td> 
   <td colname="col2"> <p>紋理解析度（若指定size=，則略過）。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph">屬性：：解析度</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph">錨點= </span> </a> </p> </td> 
   <td colname="col2"> <p>貼花對齊點。 </p> </td> 
   <td colname="col3"> <p>影像中心。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pos.md#reference-22c10904a0ce4c8bb41c2c78104221b8" type="reference" format="dita" scope="local"> <span class="codeph"> pos= </span> </a> </p> </td> 
   <td colname="col2"> <p>相對貼花位置。 </p> </td> 
   <td colname="col3"> <p>0， 0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-opac.md#reference-136b8563da714313a9e103f4ce179c5b" type="reference" format="dita" scope="local"> <span class="codeph"> opac= </span> </a> </p> </td> 
   <td colname="col2"> <p>貼花不透明度。 </p> </td> 
   <td colname="col3"> <p>100% </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph">銳利化= </span> </a> </td> 
   <td colname="col2"> <p>銳利化。 </p> </td> 
   <td colname="col3"> <p>0 （不銳利化） </p> </td> 
  </tr> 
 </tbody> 
</table>
