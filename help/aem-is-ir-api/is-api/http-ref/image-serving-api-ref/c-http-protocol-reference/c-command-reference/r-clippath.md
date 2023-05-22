---
description: 圖層剪輯路徑。 指定當前圖層的剪輯路徑。
solution: Experience Manager
title: 剪輯路徑
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86c87cd1-6e08-40cb-80e6-35a9f49b6572
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '544'
ht-degree: 0%

---

# 剪輯路徑{#clippath}

圖層剪輯路徑。 指定當前圖層的剪輯路徑。

`clipPath= *`pathDefinition`*`

`clipPathE= *`路徑名`*&#42;[, *`路徑名`*]`

<table id="simpletable_275E2A5FAB804C6388BD110D2ACA3C82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>路徑資料。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 路徑名</span></span> </p> </td> 
  <td class="stentry"> <p>層源影像中嵌入的路徑的名稱（僅限ASCII）。 </p></td> 
 </tr> 
</table>

位於由定義的區域外的層的任何部分 `clipPath=` 變為透明。

`*`路徑名`*` 是層源影像中嵌入的路徑的名稱。 該路徑被自動變換以保持與影像內容的相對對準。 如果多個 `*`路徑名`*` 指定時，伺服器會將影像剪輯到這些路徑的交集。 任意 `*`路徑名`*` 將忽略源映像中未找到的內容。

>[!NOTE]
>
>僅支援ASCII字串 `*`路徑名`*`。

`*`pathDefinition`*` 允許在圖層像素坐標中指定顯式路徑資料。

如果 `size=` 指定而不是0,0，則定位層。 在這種情況下，路徑坐標相對於圖層矩形的左上角，並基於 `origin=` 或預設值。 路徑在圖層矩形外的任何區域都保持透明。

如果 `size=` 未為純色或文本圖層指定，則該圖層會被視為自調整大小，而路徑的大小將決定其大小。 如果 `origin=` 未指定，它預設為(0,0)路徑坐標空間。 這有效地允許相對於層0的原點指定路徑坐標。

>[!NOTE]
>
>`scale=`。 `rotate=`, `anchor=` 不允許自調整實色層大小的命令。

`*`pathDefinition`*` 接受與 `d=` SVG `<path>` 元素，但是使用逗號而不是空格來分隔值。 `*`pathDefinition`*` 可以包括一個或多個閉環子路徑。

中支援以下路徑命令 `*`pathDefinition`*`:

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
   <td> <b> M</b> <span class="varname"> x,y</span> </td> 
   <td> <p> 絕對 </p> </td> 
   <td> <p> 在x,y處啟動新子路徑。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> 米</b> <span class="varname"> x,y</span> </td> 
   <td> <p> 相對 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> L</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> 直線絕對 </p> </td> 
   <td> <p> 從當前位置繪製一條線到x,y。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> 1</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> 相對線 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> C</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> 絕對 </p> </td> 
   <td> <p> 從當前位置繪製Bezier曲線到x,y。x1,y1是曲線開始處的控制點，x2,y2是曲線結束處的控制點。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> c</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> 臨時 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> Z</b> | <b>z</b> </td> 
   <td> <p> 閉合路徑 </p> </td> 
   <td> <p> 用直線關閉當前子路徑。 </p> </td> 
  </tr> 
 </tbody> 
</table>

大寫命令表示坐標值位於絕對像素位置（相對於圖層矩形的左上角）。 像素偏移跟隨相對於當前位置的小寫命令。

「m」或「M」始終會啟動新子路徑。 如果在末尾未指定「Z」或「z」，則子路徑會自動關閉（使用直線）。

如果子路徑以相對移動(&#39;m&#39;)開頭，則它相對於以下選項之一：

* 上一個子路徑的起始點（如果用「z」或「Z」關閉）。
* 前一個子路徑的終點（如果未顯式關閉）。
* 0,0，如果這是第一個子路徑。

## 屬性 {#section-d4127db0dac54e3cbd44f7ea1e001960}

層屬性。 應用於當前圖層或複合影像 `layer=comp`。 效果層忽略它。

`clipPathE=` 如果在圖層源映像中找不到具有指定名稱的路徑，或者圖層源不是映像，則忽略該路徑。

## 預設 {#section-076c35ea37fa4a44ada253b4c2dec1dd}

無，不附加圖層修剪。

## 另請參閱 {#section-dd8110fb6f5c45eba6284c5ec5f49056}

[clipXpath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clipxpath.md#reference-17e5e4da3e044943af8f963f58a45f53) 。 [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef) 。 [擴展=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
