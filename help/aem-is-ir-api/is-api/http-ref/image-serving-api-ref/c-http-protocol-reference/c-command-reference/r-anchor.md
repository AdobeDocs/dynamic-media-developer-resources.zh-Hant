---
description: 影像錨點。 在應用轉換(crop=、scale=、rotate=、flip=)之前，定義影像、實色或文本邊界框矩形的錨點。 也可作為旋轉的旋轉中心=。
solution: Experience Manager
title: 錨記
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: f62ae048-0dcc-4e93-a9f1-2e4db6bef51f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 3%

---

# 錨記{#anchor}

影像錨點。 在應用轉換(crop=、scale=、rotate=、flip=)之前，定義影像、實色或文本邊界框矩形的錨點。 也可作為旋轉的旋轉中心=。

`anchor= *`坐標`*`

`anchorN= *`coordN`*`

<table id="simpletable_3ED1CD0BF473439FA1132FC84B4452A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 坐標</span> </span> </p> </td> 
  <td class="stentry"> <p>源影像左上角的像素偏移(int、int) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p>從源影像中心歸一化的偏移（實、實） </p></td> 
 </tr> 
</table>

該錨點隨影像一起轉換，並成為層原點（除非也指定了`origin=`，在這種情況下，`anchor=`僅用作`rotate=`的旋轉中心）。

`anchorN=0,0` 將影像錨點置於源影像的中心。`anchorN=-0.5,-0.5` 或 `anchor=0,0` 者位於左上角， `anchorN=0.5,0.5` 而位於源影像的右下角。

## 屬性 {#section-f08942bc6aae46a8b5d341faaff80640}

源影像屬性。 應用於當前層，如果`layer=comp`則應用於層0。

## 預設 {#section-35d369fab1254f1a9b91684a6e169ad1}

如果未指定`anchor=`，則使用catalog::Anchor。 如果未定義`catalog::Anchor`，則使用影像矩形的中心（與指定`anchorN=0,0`相同）。

涉及`textPs=`的文本層和涉及`clipPath=`的圖層可以具有不同的預設錨點。

## 範例 {#section-cc127e6b1ea94524900b5c0dd8b4c7ec}

請參閱[範本](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)中的「範例C」。

## 另請參閱 {#section-9877ea3a0743492aaa4fa1dfc9510b07}

[目錄：：錨點](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-anchor-cat.md) , [原點=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138), [旋轉=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096), [剪輯路徑=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d),  [文字層](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
