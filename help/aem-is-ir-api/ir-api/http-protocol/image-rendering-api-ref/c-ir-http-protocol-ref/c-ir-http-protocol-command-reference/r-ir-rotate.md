---
title: 旋轉
description: 材料旋轉角。 定義材料的旋轉角。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 355d9691-c04b-44a6-9563-5bef185cfa7e
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 7%

---

# 旋轉{#rotate}

材料旋轉角。 定義材料的旋轉角。

` rotate= *`角度`*`

<table id="simpletable_F1A87ECD86E8429788825374A6882CB9"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 角度 </span> </p> </td> 
  <td class="stentry"> <p>旋轉角度(度（實數）)。 </p> </td> 
 </tr> 
</table>

將可重複的紋理材料（不包括壁紙）旋轉45°倍，以應用於「平整對象」或「平面對象」。

在應用於「流線」和「草繪對象」時，按任意角度旋轉可重複紋理材料。

以任意角度旋轉貼花材料。

正角順時針旋轉。 紋理或貼花圍繞錨點旋轉( `anchor=`);錨點仍與目標對象的原點對齊。

## 屬性 {#section-ad4d07897ca24f63af1a4062f8618e36}

物料屬性。 被純色、牆紙、機櫃和窗戶處理材料忽略。 *`angle`* 對於可重複紋理，必須是45的倍數，除非應用於「流線」或「草繪對象」。

## 預設 {#section-14c991e71b74449db8ff18a775949b28}

`rotate=0`的雙曲餘切值。

## 另請參閱 {#section-f73c00e9368b478dac1fd15bb4367a12}

[錨記=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
