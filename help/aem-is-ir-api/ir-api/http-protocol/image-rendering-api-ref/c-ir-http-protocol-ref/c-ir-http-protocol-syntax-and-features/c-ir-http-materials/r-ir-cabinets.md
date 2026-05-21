---
title: 檔案櫃
description: 檔案櫃材料指定檔案櫃樣式檔案（.vnc副檔名），這是一個特殊的資料檔案，其中包含檔案櫃的攝影表示以及引數配置圖定義及呈現檔案櫃正面所需的其他資訊。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cdb3ed5e-c396-483d-aea0-2b3f24efe56e
TQID: 'https://experienceleague.adobe.com/SzkFcvt2K-pHseOvk42kwWVaIl2-BnQK8aSEwSTB9zA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 159
ht-degree: 3%

---

# 檔案櫃{#cabinets}

檔案櫃材料指定檔案櫃樣式檔案（.vnc副檔名），這是一個特殊的資料檔案，其中包含檔案櫃的攝影表示以及引數配置圖定義及呈現檔案櫃正面所需的其他資訊。

[!DNL vnc]檔案可能包含可重複的木紋紋理，或紋理可以透過第二個引數提供到外部`src=`。 某些[!DNL vnc]檔案允許對機櫃正面選取的區域進行彩色化或紋理化（通常用於層壓機櫃樣式）。

機櫃材料只能套用至機櫃物件。

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
   <td colname="col2"> <p>封包樣式檔案；必填。 </p> </td> 
   <td colname="col3"> <p>無。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>選用的紋理影像檔（<span class="codeph"> src= </span>的第二個值）。 </p> </td> 
   <td colname="col3"> <p>無。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph">資源= </span> </a> </p> </td> 
   <td colname="col2"> <p>選用的紋理解析度。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph">屬性：：解析度</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa" type="reference" format="dita" scope="local"> <span class="codeph">色彩= </span> </a> </p> </td> 
   <td colname="col2"> <p>為機櫃和/或紋理上色。 </p> </td> 
   <td colname="col3"> <p>無。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph">銳利化= </span> </a> </p> </td> 
   <td colname="col2"> <p>銳利化。 </p> </td> 
   <td colname="col3"> <p>0 （不銳利化） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-flags.md#reference-3a4844f0f21346d79e6508aaad9a9ac9" type="reference" format="dita" scope="local"> <span class="codeph">旗標= </span> </a> </p> </td> 
   <td colname="col2"> <p>特殊轉譯器旗標。 </p> </td> 
   <td colname="col3"> <p>0 （無旗標） </p> </td> 
  </tr> 
 </tbody> 
</table>
