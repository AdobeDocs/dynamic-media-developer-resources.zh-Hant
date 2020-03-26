---
description: 套用旗標。 指定其他演算選項。
seo-description: 套用旗標。 指定其他演算選項。
seo-title: 標幟
solution: Experience Manager
title: 標幟
topic: Scene7 Image Serving - Image Rendering API
uuid: 43ed24fe-461e-4973-aa44-8fba66668e6f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 標幟{#flags}

套用旗標。 指定其他演算選項。

`flags= *`val`*`

<table id="simpletable_00B21BD9E47E4D2FB0042CB507431916"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>標籤值。 </p></td> 
 </tr> 
</table>

目前僅用於機櫃材料。

`flags=0` （預設）將上部機櫃呈現為實體門。

`flags=1` 使用玻璃門轉換上櫃（如果暗角是用玻璃門製作的）。

## 屬性 {#section-a2b00d7bb15e449ea85178acb92d8285}

材料屬性。 如果不是機櫃材料，或者目標機櫃對象不允許玻璃門，則忽略。

## 預設 {#section-4c134b02a1da4ffb9841233f98f6e97c}

`flags=0` 沒有玻璃門。
