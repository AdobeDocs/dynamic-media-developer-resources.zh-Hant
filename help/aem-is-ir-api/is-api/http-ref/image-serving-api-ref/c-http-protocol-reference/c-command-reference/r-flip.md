---
description: 翻轉層。 在套用裁切=和之後，在旋轉=和延伸=之前，水準、垂直或兩者翻轉圖層。
solution: Experience Manager
title: 翻轉
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 451d8b4d-0f22-41f3-ac86-435797c23ea3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 3%

---

# 翻轉{#flip}

翻轉層。 在套用裁切=和之後，在旋轉=和延伸=之前，水準、垂直或兩者翻轉圖層。

`flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> l  </span> </p> </td> 
  <td class="stentry"> <p>水準（左 — 右）翻轉圖層。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ud  </span> </p> </td> 
  <td class="stentry"> <p>垂直翻轉圖層（上下）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lrud  </span> </p> </td> 
  <td class="stentry"> <p>水準和垂直翻轉。 </p> </td> 
 </tr> 
</table>

也可套用至文字層。

選擇`layer=comp`時，某些命令（包括`extend=`）將隱式應用於層0而非複合層。 在這種情況下，自動分配給第0層的所有命令都將在應用於`layer=comp`的命令之前應用。 因此，當`layer=comp`時，在`flip=`之前應用`extend=`。

>[!NOTE]
>
>翻轉層基於層錨點定位；當錨點不位於層的中心時，不同的flip=值將導致不同的層位置。

## 屬性 {#section-294da2af7be746b5adfc35e29ee68217}

圖層命令。 若`layer=comp`，則套用至目前層或複合影像。 被效果層忽略。

## 預設 {#section-502044f81a89492198d5f12a738459ea}

無。

## 另請參閱 {#section-47f6484deccd420983df15ec163b4a83}

[旋轉=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) , [錨點=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
