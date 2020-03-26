---
description: 材料表面光澤度。 指定材料曲面的相對光澤度。 用於選取照明地圖並控制光澤效果和3D反射的演算。
seo-description: 材料表面光澤度。 指定材料曲面的相對光澤度。 用於選取照明地圖並控制光澤效果和3D反射的演算。
seo-title: 光澤
solution: Experience Manager
title: 光澤
topic: Scene7 Image Serving - Image Rendering API
uuid: 3774e08b-d24e-4cf2-8719-32a21bb9bcb6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 光澤{#gloss}

材料表面光澤度。 指定材料曲面的相對光澤度。 用於選取照明地圖並控制光澤效果和3D反射的演算。

`gloss= *`val`*`

<table id="simpletable_82166CA080AD401180404462FB2407D7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>預設（參考）光澤值的光澤(0...100%)或-1。 </p></td> 
 </tr> 
</table>

較高的光澤值通常會導致更強、更銳利的反射，如果暈映中啟用了光澤效果，則主要通過增加照明對比來增強材料表面上的鏡面亮部。 每個材料類型( `type=`)定義最小和最大渲染效果。 對於某些材料類型（例如牆紙），對渲染效果的外觀幾乎沒有任何影響，而對於其他材料類型（例如石頭或陶瓷），效果顯著更顯著。 `gloss=`

如果 `illum=-1` 暈映定義了多個照明映射，則 `gloss=` 選擇用於當前渲染操作的照明映射。 渲染器選擇其光澤值最接近指定光澤的照明映射。

`gloss=-1` 選擇選定照明映射的參考光澤值，如暈映的視圖屬性中所定義。 這可確保照明圖的使用與編寫的完全相同，而不需進一步修改，即使光澤效果已啟用。 如果 `illum=-1` 也使用暈映視圖中第一照明地圖的參考光澤值。

## 屬性 {#section-92c20c7890fc4aad8d1725d1a1f82da6}

材料屬性。 如果暈映未定義多個照明映射，或如果指定 `illum=` ，則忽略暈映，如果暈映未包含3D反射資料，或當前對象不支援3D反射，或者如果暈映中禁用了光澤效果。

## 預設 {#section-3722fb5f85c24bc29bdf9c92ce04e678}

`attribute::Gloss` 如果材料基於目錄條目，則預設照明圖或由指定的照明圖的參考光澤值 `illum=`。

## 另請參閱 {#section-29f5b761481a4c52a499a2e16e63c70b}

[屬性：:Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb), [type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35), [rough=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180), [Glossmap=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a)[,Glossillum=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-illum.md#reference-8efe483a30684022bfe711eb73efbee6)
