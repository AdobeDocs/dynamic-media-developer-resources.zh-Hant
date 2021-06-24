---
description: 材料旋轉角度。 定義材料的旋轉角。
solution: Experience Manager
title: 旋轉
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 355d9691-c04b-44a6-9563-5bef185cfa7e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 6%

---

# 旋轉{#rotate}

材料旋轉角度。 定義材料的旋轉角。

` rotate= *`角度`*`

<table id="simpletable_F1A87ECD86E8429788825374A6882CB9"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 角度 </span> </p> </td> 
  <td class="stentry"> <p>旋轉角度（度）。 </p> </td> 
 </tr> 
</table>

應用於「平整對象」或「平面對象」時，可重複的紋理材料（不包括壁紙）旋轉45度的倍數。

應用於流線和草繪對象時，按任意角度旋轉可重複的紋理材料。

以任意角度旋轉傾斜材料。

正角度順時針旋轉。 紋理或傾斜繞錨點旋轉(`anchor=`);錨點與目標對象的源保持對齊。

## 屬性 {#section-ad4d07897ca24f63af1a4062f8618e36}

材料屬性。 被固色、牆紙、櫥櫃和窗戶處理材料忽略。 *`angle`* 必須是可重複紋理的45倍，除非應用到流線或草繪對象。

## 預設 {#section-14c991e71b74449db8ff18a775949b28}

`rotate=0`，不可旋轉。

## 另請參閱 {#section-f73c00e9368b478dac1fd15bb4367a12}

[錨記=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
