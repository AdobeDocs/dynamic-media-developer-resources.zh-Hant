---
description: 回應影像最適模式。 指定比例因子的計算方式，當指定響應大小wid=和hei=和scl=時，該比例因子用於將合成影像縮放到響應影像。
solution: Experience Manager
title: 符合
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 2%

---


# 符合{#fit}

回應影像最適模式。 指定比例因子的計算方式，當指定響應大小wid=和hei=和scl=時，該比例因子用於將合成影像縮放到響應影像。

` fit= *`Modesupcal`*, *`版`*`

<table id="simpletable_50FBDC6B7CB2448891DD0F491DEB5ACF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 模式  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> fit|constrain|crop|wrap|stretch|hfit|vfit  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 高檔  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
 </tr> 
</table>

在以下模式選項說明中，假定&#x200B;*`xScale`*&#x200B;是合成影像寬度與響應影像寬度的比值，而&#x200B;*`yScale`*&#x200B;是合成影像高度與響應影像高度的比值。

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
   <td colname="col2"> <p>縮放合成影像，使其適合使用<span class="codeph"> wid= </span>和<span class="codeph"> hei= </span>分配的空間，而且空間最小且無裁切。 回應影像的大小與<span class="codeph"> wid= </span>和<span class="codeph"> hei= </span>指定的大小完全相同。 應用<span class="varname"> xScale </span>和<span class="varname"> yScale </span>的較小值。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 約束  </span> </p> </td> 
   <td colname="col2"> <p>縮放合成影像，如<span class="codeph">（適合</span>），使其適合<span class="codeph"> wid= </span>和<span class="codeph"> hei= </span>分配的空間，但實際響應影像可小於<span class="codeph"> wid= </span>和<span class="codeph"> hei= </span>指定的空間，以避免空間。 應用<span class="varname"> xScale </span>和<span class="varname"> yScale </span>的較小值。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 裁切 </span> </p> </td> 
   <td colname="col2"> <p>縮放合成影像，以填滿整個回應影像，而且裁切次數很少，沒有空格。 應用<span class="varname"> xScale </span>和<span class="varname"> yScale </span>的較大值。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 換行 </span> </p> </td> 
   <td colname="col2"> <p>縮放合成影像，如<span class="codeph">裁切</span>，以覆蓋整個回應影像，但實際回應影像可能比使用<span class="codeph"> wid= </span>和<span class="codeph"> hei= </span>指定的影像大，以避免裁切。 應用<span class="varname"> xScale </span>和<span class="varname"> yScale </span>的較大值。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 拉伸  </span> </p> </td> 
   <td colname="col2"> <p>以x和y單獨縮放合成影像，以填滿整個回應影像，而不會裁切，也不會加上空格。 這通常會變更影像的外觀比例。 <span class="varname"> xScale用 </span> 於水準縮放， <span class="varname"> yScale </span> 用於垂直縮放。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> hfit  </span> </p> </td> 
   <td colname="col2"> <p>套用<span class="varname"> xScale </span>以水準方式緊密配合影像，而上方和／或下方可能會有裁切或空格。 適用於特殊應用程式。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> vfit  </span> </p> </td> 
   <td colname="col2"> <p>套用<span class="varname"> yScale </span>以垂直方式調整影像，其左側和／或右側可能會有裁切或空格。 適用於特殊應用程式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

將&#x200B;*`upscale`*&#x200B;設為&#39;1&#39;可允許縮放，或將&#39;0&#39;設為限制*`xScale`*和&#x200B;*`yScale`*&#x200B;限制為1:1。 如果停用升級，如果合成影像小於回應影像，則可能會有額外的空白字元。

裁切和空格預設會置中；其位置可以用`align=`控制。 空白填色的顏色和不透明度由`bgc=`決定。

## 屬性 {#section-6d7a5a7e18434bca9bc2fdb236af8909}

檢視屬性。 不論目前的圖層設定為何，都適用。 必須至少指定`wid=`或`hei=`之一，否則傳回錯誤；必須同時指定`wid=`和`hei=`，以使適應模式如說明般運作。 當也指定`req=tmb`時，會傳回錯誤。

## 預設 {#section-3a553b4b29ef447a8331d6954f3f06da}

`fit=fit,0`

## 另請參閱 {#section-788f7e168da64fc5abf29d971a598b01}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)
