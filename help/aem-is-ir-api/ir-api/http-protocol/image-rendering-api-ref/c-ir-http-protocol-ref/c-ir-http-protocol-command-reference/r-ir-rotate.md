---
description: 材料旋轉角度。 定義材料的旋轉角度。
seo-description: 材料旋轉角度。 定義材料的旋轉角度。
seo-title: 旋轉
solution: Experience Manager
title: 旋轉
topic: Scene7 Image Serving - Image Rendering API
uuid: 497cd8ea-c6a4-45d2-b5e0-0898ac00913d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# rotate{#rotate}

材料旋轉角度。 定義材料的旋轉角度。

` rotate= *`角度`*`

<table id="simpletable_F1A87ECD86E8429788825374A6882CB9"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 角度 </span> </p> </td> 
  <td class="stentry"> <p>旋轉角度（以度為單位）。 </p> </td> 
 </tr> 
</table>

當套用至平面物件或平面物件時，可重複的紋理材質（不包括桌布）旋轉45度倍。

將可重複的紋理材料應用於流線和草繪對象時，按任意角度旋轉。

以任意角度旋轉傾斜材料。

正角度順時針旋轉。 紋理或壁片繞錨點旋轉( `anchor=`);錨點與目標對象的原點保持對齊。

## 屬性 {#section-ad4d07897ca24f63af1a4062f8618e36}

材料屬性。 被純色、壁紙、櫥櫃和窗戶處理材料所忽略。 *`angle`* 必須是45的倍數，才能產生可重複的紋理，除非套用至流線或素描物件。

## 預設 {#section-14c991e71b74449db8ff18a775949b28}

`rotate=0`，以禁止旋轉。

## 另請參閱 {#section-f73c00e9368b478dac1fd15bb4367a12}

[錨記=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
