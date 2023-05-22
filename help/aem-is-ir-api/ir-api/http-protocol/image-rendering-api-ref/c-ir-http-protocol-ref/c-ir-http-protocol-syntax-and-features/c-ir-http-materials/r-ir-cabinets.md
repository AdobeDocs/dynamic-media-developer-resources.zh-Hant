---
title: 檔案櫃
description: 機櫃材料指定機櫃樣式檔案（.vnc檔案副檔名）、包含機櫃照片表示以及參數佈局定義和繪製機櫃前面所需的其他資訊的特殊資料檔案。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cdb3ed5e-c396-483d-aea0-2b3f24efe56e
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 4%

---

# 檔案櫃{#cabinets}

機櫃材料指定機櫃樣式檔案（.vnc檔案副檔名）、包含機櫃照片表示以及參數佈局定義和繪製機櫃前面所需的其他資訊的特殊資料檔案。

[!DNL vnc] 檔案可以包括可重複的木紋紋理，或者可以通過第二參數向外部提供紋理 `src=`。 確定 [!DNL vnc] 檔案允許對機櫃前面的選定區域進行彩色化或紋理化（通常用於層壓板機櫃樣式）。

機櫃材料只能應用於機櫃對象。

<table id="table_0B16200886FE4DFEBB1E4BE8FBA67EE4"> 
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
   <td colname="col2"> <p>檔案櫃樣式檔案；。 </p> </td> 
   <td colname="col3"> <p>無。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>可選紋理影像檔案(第二個值 <span class="codeph"> src= </span>)。 </p> </td> 
   <td colname="col3"> <p>無。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> 雷斯= </span> </a> </p> </td> 
   <td colname="col2"> <p>可選紋理解析度。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> 屬性：：解析度 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa" type="reference" format="dita" scope="local"> <span class="codeph"> 顏色= </span> </a> </p> </td> 
   <td colname="col2"> <p>著色機櫃和/或紋理。 </p> </td> 
   <td colname="col3"> <p>無。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> 急= </span> </a> </p> </td> 
   <td colname="col2"> <p>銳利化. </p> </td> 
   <td colname="col3"> <p>0（無銳化） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-flags.md#reference-3a4844f0f21346d79e6508aaad9a9ac9" type="reference" format="dita" scope="local"> <span class="codeph"> 標誌= </span> </a> </p> </td> 
   <td colname="col2"> <p>特殊渲染標誌。 </p> </td> 
   <td colname="col3"> <p>0（無標誌） </p> </td> 
  </tr> 
 </tbody> 
</table>
