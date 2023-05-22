---
title: 合
description: 響應影像適合模式。 指定如何計算比例因子，當用wid=和hei=和scl=指定響應大小時，該比例因子用於將複合影像縮放到響應影像。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d2939f86-5dab-471d-ba59-70d91ae1e4fd
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 1%

---

# 合{#fit}

響應影像適合模式。 指定如何計算比例因子，當用wid=和hei=和scl=指定響應大小時，該比例因子用於將複合影像縮放到響應影像。

` fit= *`模式`*, *`高檔`*`

<table id="simpletable_50FBDC6B7CB2448891DD0F491DEB5ACF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 模式 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> fit|constrain|crob|crow|stret|hfit|vfit </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 高檔 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
 </tr> 
</table>

在以下模式選項說明中，假定 *`xScale`* 是複合影像寬度與響應影像寬度的比值， *`yScale`* 是合成影像高度與響應影像高度的比值。

<table id="table_33408ECA9D164AFAA249F8589060545E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 參數 </th> 
   <th colname="col2" class="entry"> 定義 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 合 </span> </p> </td> 
   <td colname="col2"> <p>縮放複合影像，使其適用於 <span class="codeph"> wid= </span> 和 <span class="codeph"> 黑= </span>以及最小的空白和無裁剪。 響應影像的大小將與 <span class="codeph"> wid= </span> 和 <span class="codeph"> 黑= </span>。 小於 <span class="varname"> x縮放 </span> 和 <span class="varname"> 比例 </span> 的子菜單。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 約束 </span> </p> </td> 
   <td colname="col2"> <p>將複合影像縮放 <span class="codeph"> 合 </span> 這樣它就能適應 <span class="codeph"> wid= </span> 和 <span class="codeph"> 黑= </span>，但實際響應影像可能小於 <span class="codeph"> wid= </span> 和 <span class="codeph"> 黑= </span> 以避免白空。 小於 <span class="varname"> x縮放 </span> 和 <span class="varname"> 比例 </span> 的子菜單。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 作物 </span> </p> </td> 
   <td colname="col2"> <p>縮放複合影像，以填充整個響應影像，同時裁剪最少且沒有空格。 大 <span class="varname"> x縮放 </span> 和 <span class="varname"> 比例 </span> 的子菜單。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 換行 </span> </p> </td> 
   <td colname="col2"> <p>將複合影像縮放 <span class="codeph"> 作物 </span> 這樣它覆蓋整個響應影像，但實際響應影像可能比指定的 <span class="codeph"> wid= </span> 和 <span class="codeph"> 黑= </span> 以免下落。 大 <span class="varname"> x縮放 </span> 和 <span class="varname"> 比例 </span>的子菜單。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 拉 </span> </p> </td> 
   <td colname="col2"> <p>以x和y獨立縮放複合影像，以填充整個響應影像，而不會裁剪和不會顯示空白。 這通常會更改影像的長寬比。 <span class="varname"> x縮放 </span> 用於水準縮放和 <span class="varname"> 比例 </span> 垂直縮放。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 肥 </span> </p> </td> 
   <td colname="col2"> <p>應用 <span class="varname"> x縮放 </span> 可以在頂部和/或底部剪切或空白，使影像在水準方向上緊密對齊。 適用於特殊應用。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 小 </span> </p> </td> 
   <td colname="col2"> <p>應用 <span class="varname"> 比例 </span> 垂直調整影像，左邊和/或右邊可能有裁剪或空白。 適用於特殊應用。 </p> </td> 
  </tr> 
 </tbody> 
</table>

設定 *`upscale`* 「1」允許升級或限制為「0」*`xScale`*和 *`yScale`* 限制為1:1。 如果禁用了上縮放，則如果複合影像小於響應影像，則可能存在附加的空白。

預設情況下，裁剪和空白居中；他們的位置可以 `align=`。 空白填充的顏色和不透明度由 `bgc=`。

## 屬性 {#section-6d7a5a7e18434bca9bc2fdb236af8909}

查看屬性。 無論當前圖層設定如何都適用。 其中至少一個 `wid=` 或 `hei=` 必須同時指定，否則返回錯誤；兩者 `wid=` 和 `hei=` 必須指定適合模式才能按說明行事。 當 `req=tmb` 。

## 預設 {#section-3a553b4b29ef447a8331d6954f3f06da}

`fit=fit,0`

## 另請參閱 {#section-788f7e168da64fc5abf29d971a598b01}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) 。 [黑=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)。 [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)。 [對齊=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)
