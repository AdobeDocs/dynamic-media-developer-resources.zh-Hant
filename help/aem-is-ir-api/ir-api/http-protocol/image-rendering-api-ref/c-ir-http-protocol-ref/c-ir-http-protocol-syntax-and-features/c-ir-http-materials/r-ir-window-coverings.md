---
description: 窗蓋材料包括軟窗蓋（窗簾、窗閥、咖啡窗簾）和硬窗蓋（窗簾和百葉窗）。
solution: Experience Manager
title: 窗口覆蓋
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: ce6543a1-2438-4661-95bf-ff3d956013bc
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 3%

---

# 窗口覆蓋{#window-coverings}

窗蓋材料包括軟窗蓋（窗簾、窗閥、咖啡窗簾）和硬窗蓋（窗簾和百葉窗）。

覆蓋材料的窗口指定了覆蓋樣式檔案&#x200B;*（[!DNL .vnw]檔案副檔名）的*&#x200B;窗口，與暈映類似的特殊資料檔案，包含掩模、照明、佈局以及定義窗口覆蓋的紋理資料。

[!DNL vnw] 檔案不包括窗口覆蓋的顏色和紋理（結構）。此資訊會個別指定，類似於可重複的紋理。

窗口覆蓋材料只能應用於窗口覆蓋框架對象，這些對象是重疊的對象。

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src=  </span> </a> </p> </td> 
   <td colname="col2"> <p>窗口覆蓋樣式檔案；必填。 </p> </td> 
   <td colname="col3"> <p>無。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src=  </span> </a> </p> </td> 
   <td colname="col2"> <p>紋理影像檔案（<span class="codeph"> src= </span>的第二個值）。 </p> </td> 
   <td colname="col3"> <p>無。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res=  </span> </a> </p> </td> 
   <td colname="col2"> <p>紋理解析度。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> 屬性：：解析度  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> 重複=  </span> </a> </p> </td> 
   <td colname="col2"> <p>重複模式。 </p> </td> 
   <td colname="col3"> <p>0（直重複） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa" type="reference" format="dita" scope="local"> <span class="codeph"> color=  </span> </a> </p> </td> 
   <td colname="col2"> <p>實色（或著色紋理）。 </p> </td> 
   <td colname="col3"> <p>128（中性灰色） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp=  </span> </a> </p> </td> 
   <td colname="col2"> <p>銳利化. </p> </td> 
   <td colname="col3"> <p>0（無銳利化） </p> </td> 
  </tr> 
 </tbody> 
</table>
