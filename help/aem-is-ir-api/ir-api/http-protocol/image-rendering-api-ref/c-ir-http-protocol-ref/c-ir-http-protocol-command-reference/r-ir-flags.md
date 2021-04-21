---
description: 套用旗標。 指定其他演算選項。
solution: Experience Manager
title: 標幟
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 5%

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
