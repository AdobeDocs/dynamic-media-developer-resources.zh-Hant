---
title: 貼花
description: 貼花材料包括諸如貼花、T恤印花和繡花或印花標誌等服裝結構。 它還包括在內部或外部應用中使用的非可重複的平面物體，如區域地毯、壁掛藝術和標誌。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 07190abd-9f6f-46b5-bf77-cd97c48fc9be
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 3%

---

# 貼花{#decals}

貼花材料包括諸如貼花、T恤印花和繡花或印花標誌等服裝結構。 它還包括在內部或外部應用中使用的非可重複的平面物體，如區域地毯、壁掛藝術和標誌。

如果材料是在貼花MSS中指定的，則它被視為貼花。 貼花圖案通常是RGBA影像，其α通道定義貼花圖案的形狀。

可以將一個貼面應用於每個平整、流線、草繪、平面或壁對象（除非設定「無紋理」標誌）。 貼花通過對準貼花的 `anchor=` 與vignette對象的傾斜原點。 該位置可進一步調整 `pos=`。

如果貼花材料定義厚度，而貼花對象定義光向量，則呈現投影。

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
   <td colname="col2"> <p>影像（通常使用Alpha）;。 </p> </td> 
   <td colname="col3"> <p>無。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988" type="reference" format="dita" scope="local"> <span class="codeph"> 大小= </span> </a> </p> </td> 
   <td colname="col2"> <p>傾斜寬度、高度和厚度（用於投影）。 </p> </td> 
   <td colname="col3"> <p> <span class="varname"> 影像寬度 </span> x <span class="codeph"> 雷 </span>。 <span class="varname"> imageHeight </span> x <span class="codeph"> res,0 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> 雷斯= </span> </a> </p> </td> 
   <td colname="col2"> <p>紋理解析度（如果指定size=，則忽略）。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> 屬性：：解析度 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> 錨= </span> </a> </p> </td> 
   <td colname="col2"> <p>傾斜對齊點。 </p> </td> 
   <td colname="col3"> <p>影像中心。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pos.md#reference-22c10904a0ce4c8bb41c2c78104221b8" type="reference" format="dita" scope="local"> <span class="codeph"> pos= </span> </a> </p> </td> 
   <td colname="col2"> <p>相對傾斜位置。 </p> </td> 
   <td colname="col3"> <p>0, 0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-opac.md#reference-136b8563da714313a9e103f4ce179c5b" type="reference" format="dita" scope="local"> <span class="codeph"> opac= </span> </a> </p> </td> 
   <td colname="col2"> <p>戴爾不透明。 </p> </td> 
   <td colname="col3"> <p>100% </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> 急= </span> </a> </td> 
   <td colname="col2"> <p>銳利化. </p> </td> 
   <td colname="col3"> <p>0（無銳化） </p> </td> 
  </tr> 
 </tbody> 
</table>
