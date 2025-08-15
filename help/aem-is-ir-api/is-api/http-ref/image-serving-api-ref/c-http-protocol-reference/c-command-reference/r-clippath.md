---
title: 剪裁路徑
description: 圖層剪裁路徑。 指定目前圖層的剪裁路徑。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86c87cd1-6e08-40cb-80e6-35a9f49b6572
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 0%

---

# 剪裁路徑{#clippath}

圖層剪裁路徑。 指定目前圖層的剪裁路徑。

`clipPath= *`pathDefinition`*`

`clipPathE= *`pathName`*&#42;[, *`pathName`*]`

<table id="simpletable_275E2A5FAB804C6388BD110D2ACA3C82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>路徑資料。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span></span> </p> </td> 
  <td class="stentry"> <p>嵌入圖層來源影像中的路徑名稱（僅限ASCII）。 </p></td> 
 </tr> 
</table>

落在由`clipPath=`定義區域之外的圖層任何部分都會呈現為透明。

`*`pathName`*`是內嵌在圖層來源影像中的路徑名稱。 路徑會自動轉換，以維持與影像內容相對的對齊。 如果指定了多個`*`pathName`*`，伺服器會將影像剪裁到這些路徑的交集。 在來源影像中找不到任何`*`pathName`*`都會被忽略。

>[!NOTE]
>
>`*`pathName`*`只支援ASCII字串。

`*`pathDefinition`*`允許以圖層畫素座標指定明確的路徑資料。

如果指定了`size=`而非0,0，則會將圖層設為預覽。 在此情況下，路徑座標會相對於圖層矩形的左上角，而圖層會根據`origin=`或其預設來定位。 圖層矩形之外的任何路徑區域都會保持透明。

如果未指定純色或文字圖層的`size=`，則會將該圖層視為根據決定其大小的路徑範圍來調整大小。 如果未指定`origin=`，則預設為路徑座標空間的(0,0)。 此工作流程流程實際上允許指定相對於圖層0原點的路徑座標。

>[!NOTE]
>
>不允許`scale=`、`rotate=`和`anchor=`命令用於自動調整實色圖層。

`*`pathDefinition`*`接受類似於SVG `d=`專案之`<path>`屬性的值的字串，但使用逗號而非空格來分隔值。 `*`pathDefinition`*`可以包含一或多個封閉回圈子路徑。

`*`pathDefinition`*`支援下列路徑命令：

<table id="table_A74DD7A48B1C417D9D4BA46BECEAB981"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>命令</b> </th> 
   <th class="entry"> <b>名稱</b> </th> 
   <th class="entry"> <b>描述</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <b> M</b> <span class="varname"> x，y</span> </td> 
   <td> <p> moveto absolute </p> </td> 
   <td> <p> 在x，y處開始新的子路徑。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> m</b> <span class="varname"> x，y</span> </td> 
   <td> <p> 相對移動 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> L</b> *{<span class="varname"> x，y</span>} </td> 
   <td> <p> 直線至絕對 </p> </td> 
   <td> <p> 從目前位置繪製一條直線到x，y。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> l</b> *{<span class="varname"> x，y</span>} </td> 
   <td> <p> 相對線條 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> C</b> *{<span class="varname"> x1，y1，x2，y2，x，y</span>} </td> 
   <td> <p> curveto absolute </p> </td> 
   <td> <p> 從目前位置繪製貝茲曲線到x，y。x1，y1是曲線開始的控制點，x2，y2是曲線結束的控制點。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> c</b> *{<span class="varname"> x1，y1，x2，y2，x，y</span>} </td> 
   <td> <p> curveto相對 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> Z</b> | <b>z</b> </td> 
   <td> <p> closepath </p> </td> 
   <td> <p> 用直線封閉目前的子路徑。 </p> </td> 
  </tr> 
 </tbody> 
</table>

大寫指令表示座標值位於絕對畫素位置（相對於圖層矩形左上角）。 相對於目前位置，畫素位移會跟隨小寫指令。

&#39;M&#39;或&#39;M&#39;一律會開始新的子路徑。 如果未在結尾指定&#39;Z&#39;或&#39;z&#39;，則會自動關閉子路徑（使用直線）。

如果子路徑以相對移動(&#39;m&#39;)開頭，則為相對於下列其中一項的路徑：

* 上一個子路徑的起點（如果以「z」或「Z」關閉）。
* 前一個子路徑的終點（如果未明確關閉）。
* 0,0，如果它是第一個子路徑。

## 屬性 {#section-d4127db0dac54e3cbd44f7ea1e001960}

圖層屬性。 套用至目前的圖層或複合影像（若為`layer=comp`）。 效果圖層會忽略它。

如果在圖層來源影像中找不到具有指定名稱的路徑，或圖層來源不是影像，則會忽略修飾元`clipPathE=`。

## 預設 {#section-076c35ea37fa4a44ada253b4c2dec1dd}

「無」，表示沒有額外的圖層剪裁。

## 另請參閱 {#section-dd8110fb6f5c45eba6284c5ec5f49056}

[clipXpath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clipxpath.md#reference-17e5e4da3e044943af8f963f58a45f53) ， [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef) ， [延伸=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
