---
title: 剪裁路徑
description: 圖層剪裁路徑。 指定目前圖層的剪裁路徑。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86c87cd1-6e08-40cb-80e6-35a9f49b6572
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '548'
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

落在所定義區域之外的圖層任何部分 `clipPath=` 呈現為透明。

`*`pathName`*` 是內嵌在圖層來源影像中的路徑名稱。 路徑會自動轉換，以維持與影像內容相對的對齊。 如果超過一個 `*`pathName`*` 指定後，伺服器會將影像裁剪到這些路徑的交集。 任何 `*`pathName`*` 在來源影像中找不到，會忽略。

>[!NOTE]
>
>僅支援ASCII字串 `*`pathName`*`.

`*`pathDefinition`*` 允許以圖層畫素座標指定明確的路徑資料。

如果 `size=` 指定且非0,0，則會使圖層成為持久層。 在此情況下，路徑座標會相對於圖層矩形的左上角，而圖層會根據下列基準放置 `origin=` 或其預設值。 圖層矩形之外的任何路徑區域都會保持透明。

如果 `size=` 未指定純色或文字圖層，會根據路徑範圍決定圖層大小，將圖層視為自行調整大小。 如果 `origin=` 未指定，其預設值為路徑座標空間的(0,0)。 此工作流程流程實際上允許指定相對於圖層0原點的路徑座標。

>[!NOTE]
>
>`scale=`， `rotate=`、和 `anchor=` 不允許指令用於自動調整純色圖層。

`*`pathDefinition`*` 接受類似於 `d=` SVG的屬性 `<path>` 元素，但會使用逗號來分隔值，而非空格。 `*`pathDefinition`*` 可包含一或多個封閉回圈子路徑。

下列路徑命令受到支援 `*`pathDefinition`*`：

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

圖層屬性。 套用至目前圖層或複合影像，如果 `layer=comp`. 效果圖層會忽略它。

修飾元 `clipPathE=` 如果在圖層來源影像中找不到具有指定名稱的路徑，或圖層來源不是影像，則會忽略該專案。

## 預設 {#section-076c35ea37fa4a44ada253b4c2dec1dd}

「無」，表示沒有額外的圖層剪裁。

## 另請參閱 {#section-dd8110fb6f5c45eba6284c5ec5f49056}

[clipXpath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clipxpath.md#reference-17e5e4da3e044943af8f963f58a45f53) ， [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef) ， [延伸=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
