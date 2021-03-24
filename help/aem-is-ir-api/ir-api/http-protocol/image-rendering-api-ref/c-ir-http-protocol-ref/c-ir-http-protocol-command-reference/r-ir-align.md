---
description: 紋理演算對齊方式。 指定將使用所選暈映對象定義的原點。
solution: Experience Manager
title: 對齊
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 4%

---


# align{#align}

紋理演算對齊方式。 指定將使用所選暈映對象定義的原點。

`align=0|1|2|3|4|5|6`

<table id="simpletable_D15233999E35488EB2F933BD72798E2F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>預設（中間匹配）原點。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>連續比對來源。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>隨機對齊。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3..6 </p></td> 
  <td class="stentry"> <p>使用者定義的來源。 </p></td> 
 </tr> 
</table>

渲染器將紋理應用於對象，使紋理錨點(`anchor=`)與指定的原點一致。

每個物件最多可定義6個原點(0、1、3、4、5、6)。 如果指定了`align`值，但暈映對象未定義對應的原點，則使用預設（中心匹配）原點。

`align=2` 指定隨機紋理對齊，在這種情況下 `anchor=` 會有效忽略。

主要用於裝飾材料，可能用於服裝織物，以管理相鄰物體之間的紋理對齊。

## 屬性 {#section-350fadc87dcf4812a8a02d1c3d6697a0}

材料屬性。 如果選擇了壁、機櫃、裝置或窗口覆蓋框架對象，或者材料不是可重複的紋理，則忽略此問題。

## 預設 {#section-3231c2854bae4477836b626ac208dd34}

`catalog::Alignment`，如果材料基於目錄條目，則為0（中間匹配）。

## 另請參閱 {#section-945d1ce275df487d9d564d4043156c79}

[目錄：：對齊](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) , [錨點=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
