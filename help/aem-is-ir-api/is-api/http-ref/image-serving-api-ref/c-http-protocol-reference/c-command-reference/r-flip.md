---
description: 翻轉層。 應用裁剪=和旋轉=和延伸=之前，水準、垂直或兩者翻轉圖層。
solution: Experience Manager
title: 翻轉
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 451d8b4d-0f22-41f3-ac86-435797c23ea3
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 2%

---

# 翻轉{#flip}

翻轉層。 應用裁剪=和旋轉=和延伸=之前，水準、垂直或兩者翻轉圖層。

`flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> l </span> </p> </td> 
  <td class="stentry"> <p>水準翻轉圖層（從左到右）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 美 </span> </p> </td> 
  <td class="stentry"> <p>垂直（上下）翻轉層。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 呂德 </span> </p> </td> 
  <td class="stentry"> <p>水準和垂直翻轉。 </p> </td> 
 </tr> 
</table>

也可以應用於文本圖層。

某些命令，包括 `extend=`，隱式應用於層0，而不是複合層 `layer=comp` 的子菜單。 在這種情況下，自動分配給第0層的所有命令都會應用於 `layer=comp`。 因此，當 `layer=comp`。 `extend=` 應用之前 `flip=`。

>[!NOTE]
>
>翻轉層是基於層錨點定位的；當錨點不位於圖層中心時，不同的flip=值將導致不同的圖層位置。

## 屬性 {#section-294da2af7be746b5adfc35e29ee68217}

層命令。 應用於當前圖層或複合影像 `layer=comp`。 被效果層忽略。

## 預設 {#section-502044f81a89492198d5f12a738459ea}

無。

## 另請參閱 {#section-47f6484deccd420983df15ec163b4a83}

[旋轉=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) 。 [錨=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
