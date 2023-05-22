---
title: 光澤
description: 材料表面光澤度。 指定材料曲面的相對光澤度。 用於選擇照明圖並控制光澤效果和3D反射的渲染。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6df6cd05-9462-4c1e-a7ac-efac3461cf11
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 0%

---

# 光澤{#gloss}

材料表面光澤度。 指定材料曲面的相對光澤度。 用於選擇照明圖並控制光澤效果和3D反射的渲染。

`gloss= *`谷`*`

<table id="simpletable_82166CA080AD401180404462FB2407D7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 谷</span> </span> </p></td> 
  <td class="stentry"> <p>預設（參考）光澤值的光澤(0...100%)或–1。 </p></td> 
 </tr> 
</table>

較高的光澤值通常導致更強烈、更銳利的反射，並且如果在眩光中啟用光澤效果，則主要通過增加照明對比度來增強材料表面的鏡面高光。 每種材料類型( `type=`)定義最小和最大渲染效果。 對於某些材料類型（例如，牆紙）, `gloss=` 對渲染效果外觀的任何影響最小，而對於其它材料類型（例如，石頭或陶瓷），效果顯著更顯著。

如果 `illum=-1` 如果導航器定義了多個照明圖， `gloss=` 選擇用於當前渲染操作的照明映射。 渲染器選擇其光澤值最接近指定光澤的照明圖。

`gloss=-1` 選擇所選照明映射的參考光澤值，如圖片視圖屬性中所定義。 此值確保即使啟用了光澤效果，照明圖也與創作者完全一樣使用，而無需進一步修改。 如果 `illum=-1` 然後，使用影像視圖中第一照明地圖的參考光澤值。

## 屬性 {#section-92c20c7890fc4aad8d1725d1a1f82da6}

物料屬性。 如果視頻未定義多個照明映射，則忽略。 或者，如果 `illum=` ，則視圖不包含3D反射資料。 或者，如果當前對象不支援3D反射，或者在視頻中禁用了光澤效果。

## 預設 {#section-3722fb5f85c24bc29bdf9c92ce04e678}

`attribute::Gloss` 如果材料基於目錄條目，否則預設照明圖或由指定的照明圖的參考光澤值 `illum=`。

## 另請參閱 {#section-29f5b761481a4c52a499a2e16e63c70b}

[屬性：：光澤](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb)。 [類型=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35)。 [粗=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180)。 [舌頭圖=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a)。 [伊盧姆=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-illum.md#reference-8efe483a30684022bfe711eb73efbee6)
