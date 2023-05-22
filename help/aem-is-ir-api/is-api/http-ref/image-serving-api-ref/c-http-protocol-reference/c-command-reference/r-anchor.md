---
description: 影像錨點。 在應用轉換（裁剪=、縮放=、旋轉=、flip=）之前，定義影像、實色或文本定界框矩形的錨點。 還用作旋轉的旋轉中心=。
solution: Experience Manager
title: 錨記
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f62ae048-0dcc-4e93-a9f1-2e4db6bef51f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 2%

---

# 錨記{#anchor}

影像錨點。 在應用轉換（裁剪=、縮放=、旋轉=、flip=）之前，定義影像、實色或文本定界框矩形的錨點。 還用作旋轉的旋轉中心=。

`anchor= *`坐標`*`

`anchorN= *`坐標N`*`

<table id="simpletable_3ED1CD0BF473439FA1132FC84B4452A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 坐標</span> </span> </p> </td> 
  <td class="stentry"> <p>從源影像左上角偏移的像素(int, int) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 坐標N</span> </span> </p> </td> 
  <td class="stentry"> <p>與源影像中心的歸一化偏移（實數、實數） </p></td> 
 </tr> 
</table>

錨點隨影像一起轉換並成為圖層原點(除非 `origin=` 同時指定，在這種情況下 `anchor=` 僅用作 `rotate=`)。

`anchorN=0,0` 將影像錨點置於源影像的中心。 `anchorN=-0.5,-0.5` 或 `anchor=0,0` 在左上角 `anchorN=0.5,0.5` 位於源影像的右下角。

## 屬性 {#section-f08942bc6aae46a8b5d341faaff80640}

源影像屬性。 應用於當前圖層，如果 `layer=comp`。

## 預設 {#section-35d369fab1254f1a9b91684a6e169ad1}

如果 `anchor=` 未指定，使用目錄：：錨點。 如果 `catalog::Anchor` 未定義，則使用影像矩形的中心(與指定 `anchorN=0,0`)。

涉及 `textPs=` 涉及 `clipPath=` 可能具有不同的預設錨點。

## 範例 {#section-cc127e6b1ea94524900b5c0dd8b4c7ec}

請參閱中的「示例C」 [模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)。

## 另請參閱 {#section-9877ea3a0743492aaa4fa1dfc9510b07}

[目錄：：錨點](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-anchor-cat.md) 。 [原產地=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)。 [旋轉=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096)。 [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)。 [文本圖層](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
