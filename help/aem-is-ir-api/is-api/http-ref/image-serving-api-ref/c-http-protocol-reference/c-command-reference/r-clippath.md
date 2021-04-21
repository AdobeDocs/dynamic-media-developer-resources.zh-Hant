---
description: 圖層剪輯路徑。 指定當前圖層的剪輯路徑。
solution: Experience Manager
title: clipPath
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '552'
ht-degree: 1%

---


# clipPath{#clippath}

圖層剪輯路徑。 指定當前圖層的剪輯路徑。

`clipPath= *`pathDefinition`*`

`clipPathE= *``*&#42;[, *`pathNamepathName`*]`

<table id="simpletable_275E2A5FAB804C6388BD110D2ACA3C82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>路徑資料。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span></span> </p> </td> 
  <td class="stentry"> <p>嵌入層源映像中的路徑名（僅限ASCII）。 </p></td> 
 </tr> 
</table>

位於`clipPath=`所定義區域之外的圖層的任何部分都呈現為透明。

`*``*` pathName是嵌入在層源映像中的路徑的名稱。該路徑被自動轉換以保持與影像內容的相對對齊。 如果指定了多個`*`pathName`*`，伺服器會將影像剪輯到這些路徑的交叉點。 源映像中未找到的任何`*`pathName`*`都將被忽略。

>[!NOTE]
>
>`*`pathName`*`僅支援ASCII字串。

`*`PathDefinition`*` 允許在圖層像素座標中指定顯式路徑資料。

如果指定了`size=`而不是0,0，則會定位層。 在這種情況下，路徑坐標相對於圖層矩形的左上角，並且圖層基於`origin=`或其預設設定。 圖層矩形外的路徑的任何區域都保持透明。

如果未為純色或文本圖層指定`size=`，則該圖層會根據路徑的大小決定其大小，視為自行調整大小。 如果未指定`origin=`，則預設為(0,0)路徑坐標空間。 這有效地允許相對於層0的原點指定路徑坐標。

>[!NOTE]
>
>`scale=`、 `rotate=`和命 `anchor=` 令不允許自行調整單色圖層的大小。

`*``*` pathDefinition接受與SVG元素屬性值 `d=` 類似的字 `<path>` 串，只不過使用逗號而非空格來分隔值。`*``*` pathDefinition可包含一或多個閉環子路徑。

`*`pathDefinition`*`支援以下路徑命令：

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
   <td> <b> </b> <span class="varname"> Mx,y</span> </td> 
   <td> <p> 絕對 </p> </td> 
   <td> <p> 在x,y開始新的子路徑。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> </b> <span class="varname"> mx,y</span> </td> 
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
   <td> <b> Z</b> |  <b>z</b> </td> 
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

層屬性。 如果`layer=comp`，則套用至目前圖層或複合影像。 效果圖層會忽略它。

`clipPathE=` 如果在圖層源映像中未找到具有指定名稱的路徑，或者圖層源不是映像，則忽略該路徑。

## 預設 {#section-076c35ea37fa4a44ada253b4c2dec1dd}

無，因為不會對圖層進行額外的剪裁。

## 另請參閱 {#section-dd8110fb6f5c45eba6284c5ec5f49056}

[clipXpath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clipxpath.md#reference-17e5e4da3e044943af8f963f58a45f53) ,  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef) ,  [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
