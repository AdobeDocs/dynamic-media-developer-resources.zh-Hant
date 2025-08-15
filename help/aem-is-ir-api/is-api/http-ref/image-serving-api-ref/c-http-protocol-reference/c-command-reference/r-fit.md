---
title: 符合
description: 回應影像符合模式。 指定當以wid=和hei=指定回應大小且不存在scl=時，如何計算縮放因數，以用於將複合影像縮放為回應影像。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d2939f86-5dab-471d-ba59-70d91ae1e4fd
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 1%

---

# 符合{#fit}

回應影像符合模式。 指定當以wid=和hei=指定回應大小且不存在scl=時，如何計算縮放因數，以用於將複合影像縮放為回應影像。

` fit= *`模式`*, *`升級`*`

<table id="simpletable_50FBDC6B7CB2448891DD0F491DEB5ACF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">模式</span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> fit|限制|crop|wrap|stretch|hfit|vfit </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">升級</span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
 </tr> 
</table>

在下列模式選項說明中，假設複合影像寬度與回應影像寬度的比率為&#x200B;*`xScale`*，而複合影像高度與回應影像高度的比率為&#x200B;*`yScale`*。

<table id="table_33408ECA9D164AFAA249F8589060545E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 參數 </th> 
   <th colname="col2" class="entry"> 定義 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph">符合</span> </p> </td> 
   <td colname="col2"> <p>縮放複合影像，使其符合以<span class="codeph"> wid= </span>和<span class="codeph"> hei= </span>配置的空間，具有最小的空白字元且無裁切。 回應影像具有以<span class="codeph"> wid= </span>且<span class="codeph"> hei= </span>指定的確切大小。 已套用<span class="varname"> xScale </span>和<span class="varname"> yScale </span>中的較小者。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph">限制</span> </p> </td> 
   <td colname="col2"> <p>縮放複合影像，如<span class="codeph">符合</span>，使其符合配置為<span class="codeph"> wid= </span>且<span class="codeph"> hei= </span>的空間，但實際回應影像可能小於指定<span class="codeph"> wid= </span>且<span class="codeph"> hei= </span>以避免空白。 已套用<span class="varname"> xScale </span>和<span class="varname"> yScale </span>中的較小者。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph">裁切</span> </p> </td> 
   <td colname="col2"> <p>縮放複合影像，以填滿整個回應影像，並減少裁切，而且不含空格。 已套用<span class="varname"> xScale </span>和<span class="varname"> yScale </span>中較大的值。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph">換行</span> </p> </td> 
   <td colname="col2"> <p>縮放複合影像（如<span class="codeph">裁切</span>），使其涵蓋整個回應影像，但實際回應影像可能大於以<span class="codeph"> wid= </span>和<span class="codeph"> hei= </span>指定的範圍，以避免裁切。 已套用<span class="varname"> xScale </span>和<span class="varname"> yScale </span>中較大的值。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph">延伸</span> </p> </td> 
   <td colname="col2"> <p>在x和y中獨立縮放複合影像，以填滿整個回應影像，不裁切，也不留空格。 這通常會變更影像的外觀比例。 <span class="varname"> xScale </span>用於水平縮放，而<span class="varname"> yScale </span>用於垂直縮放。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> hfit </span> </p> </td> 
   <td colname="col2"> <p>套用<span class="varname"> xScale </span>以水準緊密配合影像，頂端和/或底部可能會有裁切或空白字元。 對特殊應用程式非常有用。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> vfit </span> </p> </td> 
   <td colname="col2"> <p>套用<span class="varname"> yScale </span>以垂直緊密配合影像，可能在左側和/或右側裁切或留空白。 對特殊應用程式非常有用。 </p> </td> 
  </tr> 
 </tbody> 
</table>

將&#x200B;*`upscale`*&#x200B;設為&#39;1&#39;以允許升級，或設為&#39;0&#39;以限制*`xScale`*並將&#x200B;*`yScale`*&#x200B;限製為1:1。 如果停用向上縮放，則在複合影像小於回應影像時，可能會顯示額外的空白字元。

裁切和空白字元預設會置中；可以使用`align=`控制其位置。 空白填色的色彩和不透明度由`bgc=`決定。

## 屬性 {#section-6d7a5a7e18434bca9bc2fdb236af8909}

檢視屬性。 不論目前的圖層設定為何，皆會套用。 至少必須指定`wid=`或`hei=`之一，否則會傳回錯誤；必須同時指定`wid=`和`hei=`，才能讓符合模式按所述運作。 同時指定`req=tmb`時傳回錯誤。

## 預設 {#section-3a553b4b29ef447a8331d6954f3f06da}

`fit=fit,0`

## 另請參閱 {#section-788f7e168da64fc5abf29d971a598b01}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ， [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)， [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)， [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)
