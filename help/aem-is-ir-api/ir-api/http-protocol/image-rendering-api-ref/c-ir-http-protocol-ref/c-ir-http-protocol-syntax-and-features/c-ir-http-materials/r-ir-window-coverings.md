---
description: 窗簾材料包括柔軟的窗簾（窗簾、窗簾、咖啡窗簾）和硬的窗簾（窗簾和窗簾）。
seo-description: 窗簾材料包括柔軟的窗簾（窗簾、窗簾、咖啡窗簾）和硬的窗簾（窗簾和窗簾）。
seo-title: 窗口覆蓋
solution: Experience Manager
title: 窗口覆蓋
topic: Scene7 Image Serving - Image Rendering API
uuid: 3d74466a-b7c3-43b0-9b0b-f8bb809e2773
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Window coverings{#window-coverings}

窗簾材料包括柔軟的窗簾（窗簾、窗簾、咖啡窗簾）和硬的窗簾（窗簾和窗簾）。

窗口覆蓋材料指定 *了覆蓋樣式檔案*[!DNL .vnw] （檔案副檔名）的窗口，和類似暈映的特殊資料檔案，其中包含定義窗口覆蓋的蒙版、照明、佈局和紋理資料。

[!DNL vnw] 檔案不包含窗口覆蓋的色彩和紋理（結構）。 這些資訊會個別指定，類似於可重複的紋理。

窗口覆蓋材料只能應用於窗口覆蓋框架對象，這些對象是重疊對象。

<table id="table_545865B054E84592BDAEDA57DBFAE9B3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
   <th colname="col3" class="entry"> <p>預設 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span></a> </p> </td> 
   <td colname="col2"> <p>窗口覆蓋樣式檔案；必填。 </p> </td> 
   <td colname="col3"> <p>無。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span></a> </p> </td> 
   <td colname="col2"> <p>紋理影像檔案(src=的 <span class="codeph"> 第二個 </span>值)。 </p> </td> 
   <td colname="col3"> <p>無。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span></a> </p> </td> 
   <td colname="col2"> <p>紋理解析度。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> 屬性：：解析度 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> 重複= </span></a> </p> </td> 
   <td colname="col2"> <p>重複模式。 </p> </td> 
   <td colname="col3"> <p>0（直重複） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa" type="reference" format="dita" scope="local"> <span class="codeph"> 顏色= </span></a> </p> </td> 
   <td colname="col2"> <p>純色（或為紋理上色）。 </p> </td> 
   <td colname="col3"> <p>128（中性灰色） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> 銳= </span></a> </p> </td> 
   <td colname="col2"> <p>銳利化. </p> </td> 
   <td colname="col3"> <p>0（無銳利化） </p> </td> 
  </tr> 
 </tbody> 
</table>

