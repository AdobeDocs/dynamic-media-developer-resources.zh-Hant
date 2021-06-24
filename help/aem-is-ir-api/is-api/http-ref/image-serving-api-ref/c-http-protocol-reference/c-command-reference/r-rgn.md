---
description: 興趣地區。 指定複合影像中的矩形感興趣區域(ROI)，以像素表示。
solution: Experience Manager
title: rgn
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 4fa597ba-f949-47f2-bb0f-5c078b5c7524
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 3%

---

# rgn{#rgn}

興趣地區。 指定複合影像中的矩形感興趣區域(ROI)，以像素表示。

rgn= *`coord`*, *`size`*

<table id="simpletable_3A430F9078B04C2E90F4D1A130AFA20C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 坐標</span> </p> </td> 
  <td class="stentry"> <p>從複合影像的左上角到ROI的左上角的像素偏移(int、int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 大小</span> </p></td> 
  <td class="stentry"> <p>ROI的大小（像素）（整、整）。 </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>`rgn=` 只定義ROI而不裁切影像。當`wid=`和/或大於大小的`hei=`也被應用時，來自複合影像的附加資料可能在最終答復影像中可見。

## 屬性 {#section-53edb35f4e364d7ca13fd0886e8b0c86}

檢視屬性。 無論目前的層設定為何，都適用。

在複合影像外部延伸的ROI的任何區域都用`bgc=`填充。

`rgn=` 會在最終縮放及與、、 `scl=`、 `wid=`或相符 `hei=`之前套 `fit=` `rect=` `align=`用。

## 預設 {#section-6a3df8f670084def900ffef9dab7e94a}

整個複合影像(`rgn=0,0,width,height`)。

## 另請參閱 {#section-07883760f25c4d17aedbee36b7883891}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) ,  [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac),  [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47),  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7),  [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989),  [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3)
