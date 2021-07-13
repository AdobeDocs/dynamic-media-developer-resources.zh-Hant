---
description: 對高級文本格式使用以下命令。
solution: Experience Manager
title: 進階文字格式
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd0e94dc-34ce-4fc1-8d52-f8647c8312b8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 1%

---

# 進階文字格式{#advanced-text-formatting}

對高級文本格式使用以下命令。

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
   <td> <span class="codeph"> \dn  <span class="varname"> N  </span> </span> </td> 
   <td> <p>下標而不更改字型大小。 </p> </td> 
   <td> <p>以半點位置；預設為6。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \up  <span class="varname"> N  </span> </span> </td> 
   <td> <p>不更改字型大小的上標。 </p> </td> 
   <td> <p>以半點位置；預設為6。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \字距 <span class="varname"> N  </span> </span> </td> 
   <td> <p>按指定的字型大小禁用/啟用。 </p> </td> 
   <td> <p>半點字型大小，以上應用字距微調；0禁用字科修飾；對於在1/2點上對所有字型大小進行字距調整，預設值為1。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningoptical  </span> </td> 
   <td> <p>選擇光學字距微調。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 僅。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kernmetic  </span> </td> 
   <td> <p>選擇度量字距調整。 </p> </td> 
   <td> <p>預設. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expnd  <span class="varname"> N  </span> </span> </td> 
   <td> <p>修改字元間距。 </p> </td> 
   <td> <p>正或負四分點；預設為0。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expndtw  <span class="varname"> N  </span> </span> </td> 
   <td> <p>修改字元間距。 </p> </td> 
   <td> <p>正或負扭。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscalex  <span class="varname"> N  </span> </span> </td> 
   <td> <p>水準字元縮放。 </p> </td> 
   <td> <p>正或負百分比；預設為100。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscaley  <span class="varname"> N  </span> </span> </td> 
   <td> <p>垂直字元縮放。 </p> </td> 
   <td> <p>正或負百分比；預設為100;Dynamic Media擴充功能。 </p> <p> <span class="codeph"> \charscaley在 </span> 套用text=時也會縮 <span class="codeph"> 放行距 </span>。<span class="codeph"> textPs= </span> 無論垂直字元縮放的量多寡，都會保留行距。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ltrch  </span> </td> 
   <td> <p>選取由左至右的字元流。 </p> </td> 
   <td> <p>預設. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rtlch  </span> </td> 
   <td> <p>選取由右至左的字元流。 </p> </td> 
   <td> <p> <span class="codeph"> text= </span> 僅。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfit  <span class="varname"> N  </span> </span> </td> 
   <td> <p>啟用複製管接頭並設定允許的最大字型大小。 </p> </td> 
   <td> <p>字型大小（以半點表示）;<span class="codeph"> textPs= </span>;Dynamic Media擴充功能。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitlines  <span class="varname"> N  </span> </span> </td> 
   <td> <p>最大副檔線（軟限制）。 </p> </td> 
   <td> <p>0，不限行；<span class="codeph"> textPs= </span>;Dynamic Media擴充功能。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitmaxlines  <span class="varname"> N  </span> </span> </td> 
   <td> <p>最大副本調整線（截斷）。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 僅；Dynamic Media擴充功能。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \baselinedir  <span class="varname"> N  </span> </span> </td> 
   <td> <p>字元方向。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 僅；忽略非羅馬字型；當\stextflow <span class="codeph"> 1未 </span> 生效時忽略。 </p> <p>0垂直（預設）。 </p> <p>1順時針旋轉90度。 </p> </td> 
  </tr> 
 </tbody> 
</table>
