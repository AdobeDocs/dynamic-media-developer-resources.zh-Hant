---
title: 可重複的紋理
description: 可重複材質包括內部和外部材質，例如織物（包括服裝和室內裝飾）、牆面到牆面地板、牆紙、檯面材質、木紋材質、屋頂和側邊材質，以及任何其他一般材質。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3693498b-994a-460a-8b2e-780a1482d37a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 3%

---

# 可重複的紋理{#repeatable-textures}

可重複材質包括內部和外部材質，例如織物（包括服裝和室內裝飾）、牆面到牆面地板、牆紙、檯面材質、木紋材質、屋頂和側邊材質，以及任何其他一般材質。

可重複紋理可套用至平面、流程線、草繪、平面、壁和機櫃物件。 套用至不可紋理的物件時，該物件會以`color=`上色（如果未指定`color=`，則使用`bgc=`）。

如果材質包含指定影像的`src=`屬性，且材質發生於貼花或牆壁邊界以外的MSS中，則會視為材質。

彩現時，紋理會透過比對紋理材質的`anchor=`點與物件的紋理原點（在暈映中創作）來與物件對齊。

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
   <td colname="col2"> <p>可重複的紋理影像；必填 </p> </td> 
   <td colname="col3"> <p>無。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph">資源= </span> </a> </p> </td> 
   <td colname="col2"> <p>紋理解析度 </p> </td> 
   <td colname="col3"> <span class="codeph">屬性：：解析度</span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph">錨點= </span> </a> </p> </td> 
   <td colname="col2"> <p>紋理對齊點 </p> </td> 
   <td colname="col3"> <p>左上角。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph">重複= </span> </a> </p> </td> 
   <td colname="col2"> <p>重複模式 </p> </td> 
   <td colname="col3"> <p>0 （直接重複）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph">銳利化= </span> </a> </p> </td> 
   <td colname="col2"> <p>銳利化 </p> </td> 
   <td colname="col3"> <p>0 （無銳利化）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

除了這些基本屬性之外，可重複紋理還支援進階應用程式的下列特殊用途屬性：

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a" type="reference" format="dita" scope="local"> <span class="codeph">群組= </span> </a> </p> </td> 
   <td colname="col2"> <p>灌漿色彩和粗細；適用於陶瓷/石材瓦片材料 </p> </td> 
   <td colname="col3"> <p>群組已存在於影像中 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7" type="reference" format="dita" scope="local"> <span class="codeph">對齊= </span> </a> </p> </td> 
   <td colname="col2"> <p>對齊模式（物件之間）；用於裝飾應用程式 </p> </td> 
   <td colname="col3"> <p>置中對齊 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rotate.md#reference-3745d74a913e4065b7ac009fb4fd9e3c" type="reference" format="dita" scope="local"> <span class="codeph">旋轉= </span> </a> </p> </td> 
   <td colname="col2"> <p>紋理旋轉角度；壁物件不支援 </p> </td> 
   <td colname="col3"> <p>0 （無旋轉） </p> </td> 
  </tr> 
 </tbody> 
</table>
