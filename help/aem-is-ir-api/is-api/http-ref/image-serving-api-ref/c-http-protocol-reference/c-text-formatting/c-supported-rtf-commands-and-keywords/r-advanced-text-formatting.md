---
description: 使用以下命令進行高級文本格式設定。
solution: Experience Manager
title: 高級文本格式
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd0e94dc-34ce-4fc1-8d52-f8647c8312b8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 1%

---

# 高級文本格式{#advanced-text-formatting}

使用以下命令進行高級文本格式設定。

<table id="table_43B2EB887C0F471BB60C23B570E7D3D2"> 
 <thead> 
  <tr> 
   <th class="entry"> 命令 </th> 
   <th class="entry"> 說明 </th> 
   <th class="entry"> 附註 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \dn <span class="varname"> N </span> </span> </td> 
   <td> <p>下標而不更改字型大小。 </p> </td> 
   <td> <p>以半點位置；預設值為6。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \n <span class="varname"> N </span> </span> </td> 
   <td> <p>上標，不更改字型大小。 </p> </td> 
   <td> <p>以半點位置；預設值為6。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> 字元間距 <span class="varname"> N </span> </span> </td> 
   <td> <p>以指定字型大小禁用/啟用。 </p> </td> 
   <td> <p>字型大小（半點），在半點上應用字距微調；0禁用字距調整；對於1/2點以上的所有字型大小，預設值為1。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kernotical </span> </td> 
   <td> <p>選擇光學字距微調。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 只是。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerning度量 </span> </td> 
   <td> <p>選擇度量字距微調。 </p> </td> 
   <td> <p>預設. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expnd <span class="varname"> N </span> </span> </td> 
   <td> <p>修改字元間距。 </p> </td> 
   <td> <p>正或負四分點；預設值為0。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \exptw <span class="varname"> N </span> </span> </td> 
   <td> <p>修改字元間距。 </p> </td> 
   <td> <p>正的或負的twips。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscalex <span class="varname"> N </span> </span> </td> 
   <td> <p>水準字元縮放。 </p> </td> 
   <td> <p>正或負百分比；預設值為100。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscal <span class="varname"> N </span> </span> </td> 
   <td> <p>垂直字元縮放。 </p> </td> 
   <td> <p>正或負百分比；預設值為100;Dynamic Media分機。 </p> <p> <span class="codeph"> \charscal </span> 也可縮放線條間距， <span class="codeph"> 文本= </span>。 <span class="codeph"> textPs= </span> 始終保留行間距，而不管垂直字元縮放的大小。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ltrch </span> </td> 
   <td> <p>選擇從左到右的字元流。 </p> </td> 
   <td> <p>預設. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rtch </span> </td> 
   <td> <p>選擇從右到左的字元流。 </p> </td> 
   <td> <p> <span class="codeph"> 文本= </span> 只是。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \副本 <span class="varname"> N </span> </span> </td> 
   <td> <p>啟用複製管接頭並設定允許的最大字型大小。 </p> </td> 
   <td> <p>字型大小（半點）; <span class="codeph"> textPs= </span> 僅；Dynamic Media分機。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \折線 <span class="varname"> N </span> </span> </td> 
   <td> <p>最大複製適合線（軟限制）。 </p> </td> 
   <td> <p>0表示不限行； <span class="codeph"> textPs= </span> 僅；Dynamic Media分機。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copfitmaxlines <span class="varname"> N </span> </span> </td> 
   <td> <p>最大複製擬合線（截斷）。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 僅；Dynamic Media分機。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \baselinedir <span class="varname"> N </span> </span> </td> 
   <td> <p>字元方向。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 僅；忽略非羅馬字型；忽略 <span class="codeph"> \stextflow </span> 沒有生效。 </p> <p>0垂直（預設）。 </p> <p>1順時針旋轉90度。 </p> </td> 
  </tr> 
 </tbody> 
</table>
