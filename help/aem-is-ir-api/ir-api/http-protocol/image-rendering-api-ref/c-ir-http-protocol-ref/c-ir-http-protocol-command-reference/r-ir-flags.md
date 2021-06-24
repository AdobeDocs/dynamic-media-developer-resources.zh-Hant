---
description: 套用標幟。 指定其他渲染選項。
solution: Experience Manager
title: 標幟
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: d0c3f65e-2dec-4c35-8df4-8d111e81f3f0
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 5%

---

# 標幟{#flags}

套用標幟。 指定其他渲染選項。

`flags= *`val`*`

<table id="simpletable_00B21BD9E47E4D2FB0042CB507431916"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>標幟值。 </p></td> 
 </tr> 
</table>

目前僅用於機櫃材料。

`flags=0` （預設）使上櫃具有實體門。

`flags=1` 用玻璃門製作上櫃（如果導角是用玻璃門製作的）。

## 屬性 {#section-a2b00d7bb15e449ea85178acb92d8285}

材料屬性。 如果不是機櫃材料，或者目標機櫃對象不允許玻璃門，則忽略。

## 預設 {#section-4c134b02a1da4ffb9841233f98f6e97c}

`flags=0` 沒有玻璃門。
