---
title: 翻轉
description: 翻轉圖層。 在套用crop=和rotate=和extend=之前，水準、垂直或兩者都翻轉圖層。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 451d8b4d-0f22-41f3-ac86-435797c23ea3
TQID: 'https://experienceleague.adobe.com/7RG0rzG40Mp5eQe663S5Ayyf99SIfSLPHgqbSL2Unn4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 157
ht-degree: 2%

---

# 翻轉{#flip}

翻轉圖層。 在套用crop=和rotate=和extend=之前，水準、垂直或兩者都翻轉圖層。

`flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lr </span> </p> </td> 
  <td class="stentry"> <p>水準翻轉圖層（從左到右）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ud </span> </p> </td> 
  <td class="stentry"> <p>垂直翻轉圖層（上下翻轉）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">筆記</span> </p> </td> 
  <td class="stentry"> <p>水平與垂直翻轉。 </p> </td> 
 </tr> 
</table>

它也可以套用至文字圖層。

選取`layer=comp`時，某些命令（包括`extend=`）會隱含套用至圖層0而非複合圖層。 在這種情況下，所有自動指派給圖層0的指令都會在套用至`layer=comp`的指令之前套用。 因此，當`layer=comp`時，`extend=`在`flip=`之前套用。

>[!NOTE]
>
>翻轉的圖層會根據圖層錨點定位。 當錨點不在圖層的中央時，不同的`flip=`值會產生不同的圖層位置。

## 屬性 {#section-294da2af7be746b5adfc35e29ee68217}

圖層指令。 套用至目前的圖層或複合影像（若為`layer=comp`）。 被效果圖層忽略。

## 預設 {#section-502044f81a89492198d5f12a738459ea}

無。

## 另請參閱 {#section-47f6484deccd420983df15ec163b4a83}

[旋轉=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) ， [錨點=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
