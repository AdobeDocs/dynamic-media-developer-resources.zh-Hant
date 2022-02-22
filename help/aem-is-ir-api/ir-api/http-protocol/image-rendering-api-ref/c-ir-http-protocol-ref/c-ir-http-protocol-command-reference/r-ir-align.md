---
description: 紋理渲染對齊方式。 指定將使用由所選視頻對象定義的原點。
solution: Experience Manager
title: 對齊
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b76f173-809b-4b41-bf39-6b85f77ab2db
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 4%

---

# 對齊 {#align}

紋理渲染對齊方式。 指定將使用由所選視頻對象定義的原點。

`align=0|1|2|3|4|5|6`

<table id="simpletable_D15233999E35488EB2F933BD72798E2F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>預設（中心匹配）原點。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>連續匹配原點。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>隨機對齊。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3.6 </p></td> 
  <td class="stentry"> <p>用戶定義的源。 </p></td> 
 </tr> 
</table>

渲染器將紋理應用於對象，以便紋理錨點( `anchor=`)與指定的原點重合。

每個對象最多可定義六個原點(0、1、3、4、5、6)。 如果 `align` 指定了值，但vignette對象未定義相應的原點，則使用預設（中心匹配）原點。

`align=2` 指定隨機紋理對齊，在這種情況下 `anchor=` 被有效忽略。

主要用於裝飾材料，可能用於服裝織物，以管理相鄰物體之間紋理的對齊。

## 屬性 {#section-350fadc87dcf4812a8a02d1c3d6697a0}

物料屬性。 如果選擇了牆、機櫃、裝置或窗口覆蓋框架對象，或者材料不是可重複的紋理，則忽略該項。

## 預設 {#section-3231c2854bae4477836b626ac208dd34}

`catalog::Alignment`，如果物料基於目錄條目，則為0（中間匹配）。

## 另請參閱 {#section-945d1ce275df487d9d564d4043156c79}

[目錄：：對齊](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) 。 [錨=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
