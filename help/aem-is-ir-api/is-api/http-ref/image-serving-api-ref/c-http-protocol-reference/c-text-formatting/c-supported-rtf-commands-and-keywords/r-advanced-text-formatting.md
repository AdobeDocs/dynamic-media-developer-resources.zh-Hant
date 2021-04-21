---
description: 使用下列命令進行進階文字格式設定。
solution: Experience Manager
title: 進階的文字格式
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 1%

---


# 進階文字格式{#advanced-text-formatting}

使用下列命令進行進階文字格式設定。

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
   <td> <p>訂閱，字型大小不會變更。 </p> </td> 
   <td> <p>以半分位置；預設值為6。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \up  <span class="varname"> n  </span> </span> </td> 
   <td> <p>上標，字型大小不變。 </p> </td> 
   <td> <p>以半分位置；預設值為6。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerning  <span class="varname"> N  </span> </span> </td> 
   <td> <p>在指定的字型大小停用／啟用。 </p> </td> 
   <td> <p>字型大小（半點），以套用字距微調；0：禁用字距微調；對於半點以上所有字型大小的字距微調，預設值為1。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kernotical  </span> </td> 
   <td> <p>選擇光學字距微調。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 僅限。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kernetmic  </span> </td> 
   <td> <p>選取量度字距微調。 </p> </td> 
   <td> <p>預設. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expnd  <span class="varname"> n  </span> </span> </td> 
   <td> <p>修改字元間距。 </p> </td> 
   <td> <p>正或負四分；預設為0。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expndtw  <span class="varname"> n  </span> </span> </td> 
   <td> <p>修改字元間距。 </p> </td> 
   <td> <p>正或負扭轉。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscalex  <span class="varname"> n  </span> </span> </td> 
   <td> <p>水準字元縮放。 </p> </td> 
   <td> <p>正或負百分比；預設值為100。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscaley  <span class="varname"> n  </span> </span> </td> 
   <td> <p>垂直字元縮放。 </p> </td> 
   <td> <p>正或負百分比；預設值為100;Dynamic Media分機。 </p> <p> <span class="codeph"> \charscaley </span> 也可在套用text=時縮 <span class="codeph"> 放行距 </span>。<span class="codeph"> textPs=不 </span> 論垂直字元縮放的大小，一律會保留行距。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ltrch  </span> </td> 
   <td> <p>選擇從左到右的字元流。 </p> </td> 
   <td> <p>預設. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rtlch  </span> </td> 
   <td> <p>選擇由右至左的字元流。 </p> </td> 
   <td> <p> <span class="codeph"> text= </span> 僅。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfit  <span class="varname"> N  </span> </span> </td> 
   <td> <p>啟用複製調整並設定允許的最大字型大小。 </p> </td> 
   <td> <p>字型大小為半點；<span class="codeph"> textPs= </span>;Dynamic Media分機。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitlines  <span class="varname"> N  </span> </span> </td> 
   <td> <p>最大複製適合線（軟限制）。 </p> </td> 
   <td> <p>0表示無行限；<span class="codeph"> textPs= </span>;Dynamic Media分機。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitmaxlines  <span class="varname"> N  </span> </span> </td> 
   <td> <p>最大副本適合線（截斷）。 </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only;Dynamic Media分機。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \baselinedir  <span class="varname"> n  </span> </span> </td> 
   <td> <p>字元方向。 </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only;忽略非羅馬字型；當 <span class="codeph"> \stextflow1 </span> 無效時忽略。 </p> <p>0垂直（預設值）。 </p> <p>1順時針旋轉90度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

