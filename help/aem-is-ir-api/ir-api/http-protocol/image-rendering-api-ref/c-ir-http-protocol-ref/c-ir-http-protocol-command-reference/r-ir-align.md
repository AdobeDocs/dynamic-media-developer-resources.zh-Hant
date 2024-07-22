---
title: 對齊
description: 紋理演算對齊方式。 指定要使用所選暈映物件所定義的原點之原點。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b76f173-809b-4b41-bf39-6b85f77ab2db
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 3%

---

# 對齊 {#align}

紋理演算對齊方式。 指定要使用所選暈映物件所定義的原點之原點。

`align=0|1|2|3|4|5|6`

<table id="simpletable_D15233999E35488EB2F933BD72798E2F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>預設（置中對齊）原點。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>連續符合來源。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>隨機對齊。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3..6 </p></td> 
  <td class="stentry"> <p>使用者定義的原點。 </p></td> 
 </tr> 
</table>

轉譯器會將紋理套用至物件，讓紋理錨點( `anchor=`)與指定的原點重合。

每個物件最多可定義六個原點(0、1、3、4、5、6)。 如果指定了`align`值，但暈映物件未定義對應的原點，則會使用預設（中心比對）原點。

`align=2`指定隨機紋理對齊，在此情況下`anchor=`將被有效忽略。

主要用於室內裝飾材料，可能用於服裝織物，以管理相鄰物件之間的紋理對齊方式。

## 屬性 {#section-350fadc87dcf4812a8a02d1c3d6697a0}

材質屬性。 如果選取了壁、機櫃、裝置或視窗覆蓋物件框架物件，或者材料不是可重複的材質，則忽略該物件。

## 預設 {#section-3231c2854bae4477836b626ac208dd34}

如果素材是以目錄專案為基礎，則為`catalog::Alignment`，否則為0 （置中對齊）。

## 另請參閱 {#section-945d1ce275df487d9d564d4043156c79}

[目錄：：Alignment](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) ， [錨點=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
