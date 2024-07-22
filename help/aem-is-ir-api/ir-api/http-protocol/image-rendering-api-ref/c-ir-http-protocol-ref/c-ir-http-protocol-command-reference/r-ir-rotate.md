---
title: 旋轉
description: 材料旋轉角度。 定義材料的旋轉角度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 355d9691-c04b-44a6-9563-5bef185cfa7e
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 4%

---

# 旋轉{#rotate}

材料旋轉角度。 定義材料的旋轉角度。

` rotate= *`角度`*`

<table id="simpletable_F1A87ECD86E8429788825374A6882CB9"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">角度</span> </p> </td> 
  <td class="stentry"> <p>以度（實數）為單位的旋轉角度。 </p> </td> 
 </tr> 
</table>

套用至「平面物件」或「平面物件」時，以45度的倍數旋轉可重複的紋理材料（不包括牆紙）。

套用至「流程」和「草繪物件」時，以任意角度旋轉可重複的紋理材料。

以任意角度旋轉貼花材料。

正角度會順時針旋轉。 紋理或貼花會圍繞錨點( `anchor=`)旋轉；錨點會保持與目標物件的原點對齊。

## 屬性 {#section-ad4d07897ca24f63af1a4062f8618e36}

材質屬性。 已被純色、壁紙、機櫃和視窗處理材料忽略。 除非套用至Flowline或Sketch物件，否則可重複紋理的&#x200B;*`angle`*&#x200B;必須是45的倍數。

## 預設 {#section-14c991e71b74449db8ff18a775949b28}

`rotate=0`，無輪換。

## 另請參閱 {#section-f73c00e9368b478dac1fd15bb4367a12}

[錨點=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
