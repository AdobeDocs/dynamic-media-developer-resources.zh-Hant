---
description: 使用下列命令設定進階文字格式。
solution: Experience Manager
title: 進階文字格式
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd0e94dc-34ce-4fc1-8d52-f8647c8312b8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# 進階文字格式{#advanced-text-formatting}

使用下列命令設定進階文字格式。

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
   <td> <p>下標而不變更字型大小。 </p> </td> 
   <td> <p>位置為半點；預設為6。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \up <span class="varname"> N </span> </span> </td> 
   <td> <p>上標字型，不會變更字型大小。 </p> </td> 
   <td> <p>位置為半點；預設為6。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \字距微調<span class="varname"> N </span> </span> </td> 
   <td> <p>以指定的字型大小停用/啟用。 </p> </td> 
   <td> <p>字型大小以半點為單位，超過半點會套用字距微調；0會停用字距微調；預設為1，會將1/2點以上的所有字型大小進行字距微調。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningoptical </span> </td> 
   <td> <p>選取視覺字距微調。 </p> </td> 
   <td> <p> 僅<span class="codeph"> textPs= </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningmetric </span> </td> 
   <td> <p>選取量度字距微調。 </p> </td> 
   <td> <p>預設。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expnd <span class="varname"> N </span> </span> </td> 
   <td> <p>修改字元間距。 </p> </td> 
   <td> <p>正或負的四分之一點；預設為0。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expndtw <span class="varname"> N </span> </span> </td> 
   <td> <p>修改字元間距。 </p> </td> 
   <td> <p>正或負twip。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscalex <span class="varname"> N </span> </span> </td> 
   <td> <p>水準字元縮放。 </p> </td> 
   <td> <p>正或負百分比；預設為100。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscaley <span class="varname"> N </span> </span> </td> 
   <td> <p>垂直字元縮放。 </p> </td> 
   <td> <p>正或負百分比；預設為100；Dynamic Media擴充功能。 </p> <p> <span class="codeph"> \charscaley </span>在套用<span class="codeph">文字= </span>時也會縮放行距。 <span class="codeph"> textPs= </span>一律會保留行距，無論垂直字元縮放量為何。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ltrch </span> </td> 
   <td> <p>選取由左至右的字元流程。 </p> </td> 
   <td> <p>預設。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rtlch </span> </td> 
   <td> <p>選取由右至左的字元流程。 </p> </td> 
   <td> <p> <span class="codeph">文字=僅</span>。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfit <span class="varname"> N </span> </span> </td> 
   <td> <p>啟用複製彎管頭並設定允許的最大字型大小。 </p> </td> 
   <td> <p>字型大小以半點為單位；<span class="codeph"> textPs=僅限</span>； Dynamic Media延伸模組。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitlines <span class="varname"> N </span> </span> </td> 
   <td> <p>最大複製配合線（軟限制）。 </p> </td> 
   <td> <p>0表示無行限制；<span class="codeph"> textPs=僅限</span>； Dynamic Media延伸模組。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitmaxlines <span class="varname"> N </span> </span> </td> 
   <td> <p>最大複製符合行數（截斷）。 </p> </td> 
   <td> <p> <span class="codeph"> textPs=僅限</span>；Dynamic Media延伸模組。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \baselinedir <span class="varname"> N </span> </span> </td> 
   <td> <p>字元方向。 </p> </td> 
   <td> <p> 僅<span class="codeph"> textPs= </span>；已忽略非羅馬字型；當<span class="codeph"> \stextflow1 </span>無效時已忽略。 </p> <p>0垂直（預設）。 </p> <p>1順時針旋轉90度。 </p> </td> 
  </tr> 
 </tbody> 
</table>
