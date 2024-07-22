---
title: 光澤
description: 材質表面光澤度。 指定材料曲面的相對光澤度。 用來選取照明地圖並控制光澤效果與3D反射的彩現。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6df6cd05-9462-4c1e-a7ac-efac3461cf11
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---

# 光澤{#gloss}

材質表面光澤度。 指定材料曲面的相對光澤度。 用來選取照明地圖並控制光澤效果與3D反射的彩現。

`gloss= *`值`*`

<table id="simpletable_82166CA080AD401180404462FB2407D7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">值</span> </span> </p></td> 
  <td class="stentry"> <p>光澤值(0...100%)或–1 (預設（參考）光澤值)。 </p></td> 
 </tr> 
</table>

較高的光澤值通常會產生更強烈、更銳利的反射，而且如果在暈映中啟用光澤效果，則主要透過增加照明對比來增強材料表面的鏡面反光。 每個材質型別(`type=`)定義最小和最大演算效果。 對於某些材料型別（例如牆紙），`gloss=`對於彩現效果的外觀影響最小，而對於其他材料型別（例如石材或陶瓷），效果則明顯更明顯。

如果`illum=-1`且暈映定義了多個照明對映，`gloss=`會選取目前演算作業所使用的照明對映。 彩現器會選擇其光澤值最接近指定光澤的照明地圖。

`gloss=-1`選取選取之照明地圖的參考光澤值，如暈映的檢視屬性中所定義。 即使啟用了光澤效果，此值也能確保照度地圖完全按照編寫的方式使用，而不會進行進一步的修改。 如果`illum=-1`，則會使用暈映檢視中第一個照明地圖的參考光澤值。

## 屬性 {#section-92c20c7890fc4aad8d1725d1a1f82da6}

材質屬性。 如果暈映未定義多個照明對映，則忽略。 或者，如果指定`illum=`，暈映不包含3D反射資料。 或者，如果目前物件不支援3D反射，或者暈映中停用光澤效果。

## 預設 {#section-3722fb5f85c24bc29bdf9c92ce04e678}

`attribute::Gloss`如果材質是以目錄專案為基礎，否則會使用預設照明地圖的參考光澤值或由`illum=`指定的照明地圖。

## 另請參閱 {#section-29f5b761481a4c52a499a2e16e63c70b}

[屬性：：Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb)，[type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35)，[rough=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180)，[glossmap=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a)，[illum=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-illum.md#reference-8efe483a30684022bfe711eb73efbee6)
