---
title: 視窗涵蓋範圍
description: 窗飾材料包括柔軟的窗飾（窗簾、窗縫、咖啡館窗簾）和硬的窗飾（色調和百葉窗）。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ce6543a1-2438-4661-95bf-ff3d956013bc
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 3%

---

# 視窗涵蓋範圍{#window-coverings}

窗飾材料包括柔軟的窗飾（窗簾、窗縫、咖啡館窗簾）和硬的窗飾（色調和百葉窗）。

視窗遮蓋材料指定一個&#x200B;*視窗遮蓋樣式檔案* （[!DNL .vnw]副檔名），這是類似暈映的特殊資料檔案，包含定義視窗遮蓋的遮色片、照明、版面配置及紋理資料。

[!DNL vnw]檔案不包含視窗遮蓋的顏色和紋理（織物）。 此資訊會個別指定，類似於可重複的紋理。

視窗覆蓋材料只能套用至視窗覆蓋框架物件，這些物件是重疊的物件。

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>視窗涵蓋樣式檔案；必填。 </p> </td> 
   <td colname="col3"> <p>無。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>紋理影像檔（<span class="codeph"> src= </span>的第二個值）。 </p> </td> 
   <td colname="col3"> <p>無。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph">資源= </span> </a> </p> </td> 
   <td colname="col2"> <p>紋理解析度。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph">屬性：：解析度</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph">重複= </span> </a> </p> </td> 
   <td colname="col2"> <p>重複模式。 </p> </td> 
   <td colname="col3"> <p>0 （直接重複） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa" type="reference" format="dita" scope="local"> <span class="codeph">色彩= </span> </a> </p> </td> 
   <td colname="col2"> <p>純色（或彩色化紋理）。 </p> </td> 
   <td colname="col3"> <p>128 （中性灰色） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph">銳利化= </span> </a> </p> </td> 
   <td colname="col2"> <p>銳利化。 </p> </td> 
   <td colname="col3"> <p>0 （不銳利化） </p> </td> 
  </tr> 
 </tbody> 
</table>
