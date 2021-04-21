---
description: 翻轉圖層。 在套用crop=後和rotate=和extend=前，水準、垂直或兩者翻轉圖層。
solution: Experience Manager
title: 翻轉
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 3%

---


# flip{#flip}

翻轉圖層。 在套用crop=後和rotate=和extend=前，水準、垂直或兩者翻轉圖層。

`flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lr  </span> </p> </td> 
  <td class="stentry"> <p>水準（從左到右）翻動圖層。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ud  </span> </p> </td> 
  <td class="stentry"> <p>垂直（向上）翻轉圖層。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lrud  </span> </p> </td> 
  <td class="stentry"> <p>水準和垂直翻轉。 </p> </td> 
 </tr> 
</table>

也可套用至文字圖層。

當選取`layer=comp`時，某些命令（包括`extend=`）會隱式套用至層0，而非複合圖層。 在這種情況下，自動分配給第0層的所有命令都將在應用於`layer=comp`的命令之前應用。 因此，當`layer=comp`時，`extend=`在`flip=`之前被應用。

>[!NOTE]
>
>翻轉的圖層基於圖層錨點進行定位；當錨點不位於圖層中心時，不同的flip=值會導致不同的圖層位置。

## 屬性 {#section-294da2af7be746b5adfc35e29ee68217}

圖層命令。 如果`layer=comp`，則套用至目前圖層或複合影像。 被效果圖層忽略。

## 預設 {#section-502044f81a89492198d5f12a738459ea}

無。

## 另請參閱 {#section-47f6484deccd420983df15ec163b4a83}

[rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) ，錨 [點=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
