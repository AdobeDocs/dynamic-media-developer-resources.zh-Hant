---
title: 符合
description: 回應影像符合模式。 指定當以wid=和hei=指定回應大小且不存在scl=時，如何計算縮放因數，以用於將複合影像縮放為回應影像。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d2939f86-5dab-471d-ba59-70d91ae1e4fd
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 1%

---

# 符合{#fit}

回應影像符合模式。 指定當以wid=和hei=指定回應大小且不存在scl=時，如何計算縮放因數，以用於將複合影像縮放為回應影像。

` fit= *`模式`*, *`升級`*`

<table id="simpletable_50FBDC6B7CB2448891DD0F491DEB5ACF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 模式 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 符合|限制|裁切|換行|延伸|符合|vfit </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 升級 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
 </tr> 
</table>

在下列模式選項說明中，假設如下 *`xScale`* 是複合影像寬度與回應影像寬度的比例，而且 *`yScale`* 是複合影像高度與回應影像高度的比例。

<table id="table_33408ECA9D164AFAA249F8589060545E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 參數 </th> 
   <th colname="col2" class="entry"> 定義 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 符合 </span> </p> </td> 
   <td colname="col2"> <p>縮放複合影像，使其適合配置的空間 <span class="codeph"> wid= </span> 和 <span class="codeph"> 嘻= </span>，只有最少空白字元且無裁切。 回應影像具有指定的精確大小 <span class="codeph"> wid= </span> 和 <span class="codeph"> 嘻= </span>. 較小的 <span class="varname"> xScale </span> 和 <span class="varname"> yScale </span> 中所有規則的URL區段。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 限制 </span> </p> </td> 
   <td colname="col2"> <p>縮放複合影像，如 <span class="codeph"> 符合 </span> 以便能容納在配置的空間 <span class="codeph"> wid= </span> 和 <span class="codeph"> 嘻= </span>，但實際回應影像可能小於指定的值 <span class="codeph"> wid= </span> 和 <span class="codeph"> 嘻= </span> 以避免出現空格。 較小的 <span class="varname"> xScale </span> 和 <span class="varname"> yScale </span> 中所有規則的URL區段。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 裁切 </span> </p> </td> 
   <td colname="col2"> <p>縮放複合影像，以填滿整個回應影像，並減少裁切，而且不含空格。 較大的 <span class="varname"> xScale </span> 和 <span class="varname"> yScale </span> 中所有規則的URL區段。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 換行 </span> </p> </td> 
   <td colname="col2"> <p>縮放複合影像，如 <span class="codeph"> 裁切 </span> 因此可涵蓋整個回應影像，但實際回應影像可能大於指定的範圍 <span class="codeph"> wid= </span> 和 <span class="codeph"> 嘻= </span> 以避免裁切。 較大的 <span class="varname"> xScale </span> 和 <span class="varname"> yScale </span>中所有規則的URL區段。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 延伸 </span> </p> </td> 
   <td colname="col2"> <p>在x和y中獨立縮放複合影像，以填滿整個回應影像，不裁切，也不留空格。 這通常會變更影像的外觀比例。 <span class="varname"> xScale </span> 用於水平縮放和 <span class="varname"> yScale </span> 用於垂直縮放。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> hfit </span> </p> </td> 
   <td colname="col2"> <p>套用 <span class="varname"> xScale </span> 以水準緊密配合影像，頂端和/或底部可能會有裁切或空白字元。 對特殊應用程式非常有用。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> vfit </span> </p> </td> 
   <td colname="col2"> <p>套用 <span class="varname"> yScale </span> 以垂直緊密配合影像，並在左邊和/或右邊裁切或留空。 對特殊應用程式非常有用。 </p> </td> 
  </tr> 
 </tbody> 
</table>

設定 *`upscale`* 設為「1」以允許升級，或設為「0」以限制*`xScale`*和 *`yScale`* 限製為1:1。 如果停用向上縮放，則在複合影像小於回應影像時，可能會顯示額外的空白字元。

預設會置中裁切和空白字元，其位置可透過控制 `align=`. 空白填色的顏色和不透明度由以下專案決定 `bgc=`.

## 屬性 {#section-6d7a5a7e18434bca9bc2fdb236af8909}

檢視屬性。 不論目前的圖層設定為何，皆會套用。 至少一個 `wid=` 或 `hei=` 也必須指定，否則會傳回錯誤；兩者皆有 `wid=` 和 `hei=` 必須指定「符合」模式才能如所述運作。 發生下列情況時傳回錯誤： `req=tmb` 也會指定。

## 預設 {#section-3a553b4b29ef447a8331d6954f3f06da}

`fit=fit,0`

## 另請參閱 {#section-788f7e168da64fc5abf29d971a598b01}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ， [嘻=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)， [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)， [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)
