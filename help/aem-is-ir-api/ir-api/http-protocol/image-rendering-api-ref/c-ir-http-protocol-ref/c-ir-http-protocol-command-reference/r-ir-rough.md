---
description: 材料表面粗糙度。 指定材料曲面的相對粗糙度。
solution: Experience Manager
title: 粗
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8903b51c-c7d4-460f-8f28-00053eac9d6e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 2%

---

# 粗{#rough}

材料表面粗糙度。 指定材料曲面的相對粗糙度。

` rough= *`val`*`

<table id="simpletable_432E33EC87144AC7A2A8D9406F862708"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>表面粗糙度(0...100%)或–1以選擇預設粗糙度。 </p> </td> 
 </tr> 
</table>

用於控制3D反射渲染效果。 較低的粗糙度值通常會產生更平滑的反射效果；值越高，反射影像的隨機化和散射就越嚴重。

每種材料類型(`type=`)基於粗糙度定義最小和最大反射渲染效果。 對於某些材料類型（例如牆紙）,`rough=`幾乎不影響反射的外觀，而對於其他材料類型（例如石頭或陶瓷），影響顯著。

`rough=-1` 將粗糙度設定為伺服器內部預設值（典型材料類型為40%）。

## 屬性 {#section-515375758b254c80af576271bdb61bb8}

材料屬性。 如果暈映沒有3D反射功能，如果目標對象沒有與其關聯的3D幾何，或者目標對象沒有反映場景中的任何其他對象，則忽略。

## 預設 {#section-11861a5e6e8649ee988267d2707fd7cc}

`catalog::Roughness` 如果材料是基於目錄條目，則約40%。

## 另請參閱 {#section-d232fff7237443cc95c4bb50cb3d32bb}

[type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35) , [光澤=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
