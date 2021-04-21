---
description: 目標地區。 在合成影像中指定矩形感興趣區域(ROI)，以像素表示。
solution: Experience Manager
title: rgn
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 3%

---


# rgn{#rgn}

目標地區。 在合成影像中指定矩形感興趣區域(ROI)，以像素表示。

rgn= *`coord`*, *`size`*

<table id="simpletable_3A430F9078B04C2E90F4D1A130AFA20C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 坐標</span> </p> </td> 
  <td class="stentry"> <p>像素偏離複合影像的左上角至ROI的左上角(int, int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 大小</span> </p></td> 
  <td class="stentry"> <p>ROI的大小（以像素為單位，int、int）。 </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>`rgn=` 只定義投資報酬率，而不裁切影像。當`wid=`和／或`hei=`大於大小時，來自合成影像的額外資料可以在最終回復影像中可見。

## 屬性 {#section-53edb35f4e364d7ca13fd0886e8b0c86}

檢視屬性。 不論目前的圖層設定為何，都適用。

延伸到複合影像外部的ROI區域都會填入`bgc=`。

`rgn=` 在最終縮放和與、、、、 `scl=`、 `wid=`或配合之前應用 `hei=` `fit=` `rect=` `align=`。

## 預設 {#section-6a3df8f670084def900ffef9dab7e94a}

整個複合影像(`rgn=0,0,width,height`)。

## 另請參閱 {#section-07883760f25c4d17aedbee36b7883891}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , extend= [, extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), hei=, [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) [l=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)align= [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989) [colign, fit fit=wid=rect](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3)
