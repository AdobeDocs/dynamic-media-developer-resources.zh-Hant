---
description: 圖層剪輯路徑。 指定當前圖層的剪輯路徑。
seo-description: 圖層剪輯路徑。 指定當前圖層的剪輯路徑。
seo-title: clipPath
solution: Experience Manager
title: clipPath
topic: Scene7 Image Serving - Image Rendering API
uuid: fe84cf7a-63af-47d3-ae4f-2122f2f0a262
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# clipPath{#clippath}

圖層剪輯路徑。 指定當前圖層的剪輯路徑。

`clipPath= *`pathDefinition`*`

`clipPathE= *``*&#42;[, *`pathNamepathName`*]`

<table id="simpletable_275E2A5FAB804C6388BD110D2ACA3C82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 路 <span class="varname"> 徑定義</span></span> </p> </td> 
  <td class="stentry"> <p>路徑資料。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 路 <span class="varname"> 徑名稱</span></span> </p> </td> 
  <td class="stentry"> <p>嵌入層源映像中的路徑名（僅限ASCII）。 </p></td> 
 </tr> 
</table>

圖層中位於由定義區域外的任何部分都 `clipPath=` 會變為透明。

` *`pathName`*` 是嵌入層源映像中的路徑的名稱。 該路徑被自動轉換以保持與影像內容的相對對齊。 如果指定了多 ` *`個pathName`*` ，則伺服器會將影像剪輯到這些路徑的交叉點。 源 ` *`映像中`*` ，未找到的任何pathName都將被忽略。

>[!NOTE]
>
>pathName僅支援ASCII字 ` *`符串`*`。

` *`pathDefinition`*` 允許在圖層像素坐標中指定顯式路徑資料。

如果 `size=` 指定而非0,0，則會執行圖層。 在這種情況下，路徑坐標相對於圖層矩形的左上角，並且圖層根據或其預設來 `origin=` 定位。 圖層矩形外的路徑的任何區域都保持透明。

如果 `size=` 未為純色或文本圖層指定，則該圖層會根據路徑的大小決定其大小，視為自行調整大小。 如果 `origin=` 未指定，則預設為(0,0)路徑坐標空間。 這有效地允許相對於層0的原點指定路徑坐標。

>[!NOTE]
>
>`scale=`、 `rotate=`和命 `anchor=` 令不允許自行調整單色圖層的大小。

` *`pathDefinition`*` 接受與SVG元素屬性值類似的字串， `d=` 但 `<path>` 是使用逗號而非空格來分隔值。 ` *`pathDefinition`*` 可以包括一個或多個閉環子路徑。

pathDefinition支援以下路 ` *`徑命令`*`:

<table id="table_A74DD7A48B1C417D9D4BA46BECEAB981"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 命令</b> </th> 
   <th class="entry"> <b> 名稱</b> </th> 
   <th class="entry"> <b> 說明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <b> M</b><span class="varname"> x,y</span> </td> 
   <td> <p> 絕對 </p> </td> 
   <td> <p> 在x,y開始新的子路徑。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> m</b> <span class="varname"> x,y</span> </td> 
   <td> <p> 相對 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> L</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> line to absolute </p> </td> 
   <td> <p> 從目前位置繪製一條線至x,y。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> l</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> lineto相對 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> C</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> 絕對 </p> </td> 
   <td> <p> 從目前位置繪製貝茲曲線至x,y。x1,y1是曲線開頭的控制點，x2,y2是曲線結尾的控制點。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> c</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> 相對的 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> Z</b> | <b>z</b> </td> 
   <td> <p> 封路 </p> </td> 
   <td> <p> 使用直線關閉當前子路徑。 </p> </td> 
  </tr> 
 </tbody> 
</table>

大寫命令表示坐標值位於絕對像素位置（相對於圖層矩形的左上角）。 像素偏移會跟隨小寫命令，相對於當前位置。

&#39;m&#39;或&#39;M&#39;一律會開始新子路徑。 如果末尾未指定&#39;Z&#39;或&#39;z&#39;，子路徑會自動關閉（使用直線）。

如果子路徑以相對移動(&#39;m&#39;)開頭，則它相對於以下任一路徑：

* 上一個子路徑的起始點（如果以&#39;z&#39;或&#39;Z&#39;關閉）。
* 前一個子路徑的結束點（如果未顯式關閉）。
* 0,0，如果這是第一個子路徑。

## 屬性 {#section-d4127db0dac54e3cbd44f7ea1e001960}

層屬性。 應用於當前圖層或複合影像（如果） `layer=comp`。 效果圖層會忽略它。

`clipPathE=` 如果在圖層源映像中未找到具有指定名稱的路徑，或者圖層源不是映像，則忽略該路徑。

## 預設 {#section-076c35ea37fa4a44ada253b4c2dec1dd}

無，因為不會對圖層進行額外的剪裁。

## 另請參閱 {#section-dd8110fb6f5c45eba6284c5ec5f49056}

[clipXpath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clipxpath.md#reference-17e5e4da3e044943af8f963f58a45f53) , [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef) , [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
