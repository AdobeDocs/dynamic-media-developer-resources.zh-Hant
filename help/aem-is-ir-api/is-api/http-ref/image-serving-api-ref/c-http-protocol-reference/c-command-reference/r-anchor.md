---
description: 影像錨點。 在套用變形(crop=、scale=、rotate=、flip=)之前，定義影像、純色或文字邊界方框矩形的錨點。 也可做為旋轉=的旋轉中心。
seo-description: 影像錨點。 在套用變形(crop=、scale=、rotate=、flip=)之前，定義影像、純色或文字邊界方框矩形的錨點。 也可做為旋轉=的旋轉中心。
seo-title: 錨記
solution: Experience Manager
title: 錨記
topic: Scene7 Image Serving - Image Rendering API
uuid: 3b174360-9bb7-4dc8-83be-6b8c4ea88cd4
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# 錨記{#anchor}

影像錨點。 在套用變形(crop=、scale=、rotate=、flip=)之前，定義影像、純色或文字邊界方框矩形的錨點。 也可做為旋轉=的旋轉中心。

`anchor= *`坐標`*`

`anchorN= *`coordN`*`

<table id="simpletable_3ED1CD0BF473439FA1132FC84B4452A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 坐標</span></span> </p> </td> 
  <td class="stentry"> <p>源影像左上角的像素偏移(int, int) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span></span> </p> </td> 
  <td class="stentry"> <p>與源影像中心歸一化偏移（實數、實數） </p></td> 
 </tr> 
</table>

錨點會隨影像轉換並變成圖層原點(除非也 `origin=` 已指定，在此情 `anchor=` 況下，錨點僅用作旋轉中心 `rotate=`)。

`anchorN=0,0` 將影像錨點置於來源影像的中央。 `anchorN=-0.5,-0.5` 或 `anchor=0,0` 者位於左上角， `anchorN=0.5,0.5` 位於來源影像的右下角。

## 屬性 {#section-f08942bc6aae46a8b5d341faaff80640}

來源影像屬性。 應用於當前層，或應用於層0（如果） `layer=comp`。

## 預設 {#section-35d369fab1254f1a9b91684a6e169ad1}

如果 `anchor=` 未指定，則使用catalog::Anchor。 如果 `catalog::Anchor` 未定義，則會使用影像矩形的中心(與指定相 `anchorN=0,0`同)。

涉及文本圖層和 `textPs=` 涉及圖層的文 `clipPath=` 本圖層可具有不同的預設錨點。

## 範例 {#section-cc127e6b1ea94524900b5c0dd8b4c7ec}

請參閱範本中的「範例 [C」](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)。

## 另請參閱 {#section-9877ea3a0743492aaa4fa1dfc9510b07}

[目錄：：錨點](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-anchor-cat.md) , [原點](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)，旋 [轉=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096), [剪輯路徑=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)[，文字圖層](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
