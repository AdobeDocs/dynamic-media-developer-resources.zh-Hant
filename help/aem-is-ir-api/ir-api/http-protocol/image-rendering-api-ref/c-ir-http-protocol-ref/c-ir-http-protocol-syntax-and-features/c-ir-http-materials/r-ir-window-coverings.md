---
title: 窗蓋
description: 窗簾材料包括柔軟的窗簾（窗簾、窗簾、咖啡窗簾）和硬的窗簾（窗簾和百葉窗）。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ce6543a1-2438-4661-95bf-ff3d956013bc
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 4%

---

# 窗蓋{#window-coverings}

窗簾材料包括柔軟的窗簾（窗簾、窗簾、咖啡窗簾）和硬的窗簾（窗簾和百葉窗）。

窗口覆蓋材料指定 *窗口覆蓋樣式檔案* ( [!DNL .vnw] 檔案擴展)，類似於視頻的特殊資料檔案，包含定義窗口覆蓋的蒙版、照明、佈局和紋理化資料。

[!DNL vnw] 檔案不包括窗口覆蓋的顏色和紋理（結構）。 此資訊是單獨指定的，類似於可重複的紋理。

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>窗口覆蓋樣式檔案；。 </p> </td> 
   <td colname="col3"> <p>無。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>紋理影像檔案(第二個值 <span class="codeph"> src= </span>)。 </p> </td> 
   <td colname="col3"> <p>無。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> 雷斯= </span> </a> </p> </td> 
   <td colname="col2"> <p>紋理解析度。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> 屬性：：解析度 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> 重複= </span> </a> </p> </td> 
   <td colname="col2"> <p>重複模式。 </p> </td> 
   <td colname="col3"> <p>0（直重複） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa" type="reference" format="dita" scope="local"> <span class="codeph"> 顏色= </span> </a> </p> </td> 
   <td colname="col2"> <p>實色（或著色紋理）。 </p> </td> 
   <td colname="col3"> <p>128（中性灰色） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> 急= </span> </a> </p> </td> 
   <td colname="col2"> <p>銳利化. </p> </td> 
   <td colname="col3"> <p>0（無銳化） </p> </td> 
  </tr> 
 </tbody> 
</table>
