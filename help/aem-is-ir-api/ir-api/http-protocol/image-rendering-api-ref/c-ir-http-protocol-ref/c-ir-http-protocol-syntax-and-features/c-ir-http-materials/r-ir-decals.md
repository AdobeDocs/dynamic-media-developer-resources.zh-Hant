---
description: 貼面材料包括裝飾構件，例如應用程式、T恤印花、刺繡或印刷標誌，以及用於內部或外部應用的非可重複的平面物件，例如地毯、掛壁藝術、標誌等。
solution: Experience Manager
title: Decals
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 2%

---


# Decals{#decals}

貼面材料包括裝飾構件，例如應用程式、T恤印花、刺繡或印刷標誌，以及用於內部或外部應用的非可重複的平面物件，例如地毯、掛壁藝術、標誌等。

如果材料是在十級MSS中指定的，則該材料被視為十級。 貼牌通常是RGBA影像，其中α通道定義貼牌的形狀。

一個貼文可套用至每個平面、流線、素描、平面或壁物件（除非已設定「無紋理」標幟）。 通過將貼圖的`anchor=`與暈映對象的貼圖原點對齊，貼圖會應用到對象。 該位置可以用`pos=`進一步調整。

如果貼花材料定義厚度，而暈映對象定義光向量，則呈現下垂陰影。

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src=  </span> </a> </p> </td> 
   <td colname="col2"> <p>影像（通常為alpha）;必填。 </p> </td> 
   <td colname="col3"> <p>無。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988" type="reference" format="dita" scope="local"> <span class="codeph"> 大小=  </span> </a> </p> </td> 
   <td colname="col2"> <p>傾斜寬度、高度和厚度（用於陰影）。 </p> </td> 
   <td colname="col3"> <p> <span class="varname"> imageWidth  </span> x  <span class="codeph"> res </span>、imageHeight  <span class="varname"> x  </span>  <span class="codeph"> res、0  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res=  </span> </a> </p> </td> 
   <td colname="col2"> <p>紋理解析度（如果指定size=，則忽略）。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> 屬性：：解析度  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> 錨點=  </span> </a> </p> </td> 
   <td colname="col2"> <p>傾斜對齊點。 </p> </td> 
   <td colname="col3"> <p>影像中心。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pos.md#reference-22c10904a0ce4c8bb41c2c78104221b8" type="reference" format="dita" scope="local"> <span class="codeph"> pos=  </span> </a> </p> </td> 
   <td colname="col2"> <p>相對傾斜位置。 </p> </td> 
   <td colname="col3"> <p>0, 0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-opac.md#reference-136b8563da714313a9e103f4ce179c5b" type="reference" format="dita" scope="local"> <span class="codeph"> opac=  </span> </a> </p> </td> 
   <td colname="col2"> <p>十字不透明。 </p> </td> 
   <td colname="col3"> <p>100% </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp=  </span> </a> </td> 
   <td colname="col2"> <p>銳利化. </p> </td> 
   <td colname="col3"> <p>0（無銳利化） </p> </td> 
  </tr> 
 </tbody> 
</table>

