---
title: hei
description: 檢視高度。 指定當要求中不存在符合時回應影像（檢視影像）的高度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c812c7f0-4ac1-42cb-be47-7baebd8caf60
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 2%

---

# hei{#hei}

檢視高度。 指定當要求中不存在符合時回應影像（檢視影像）的高度。

` hei= *`val`*`

<table id="simpletable_1A36827B6E6647888A4E6E868975D716"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 變數 </span> </span> </p> </td> 
  <td class="stentry"> <p>影像高度，以畫素為單位（int大於0）。 </p> </td> 
 </tr> 
</table>

如果兩者 `wid=` 和 `scl=` 指定，複合影像可根據 `align=`屬性。 時間 `fit=` 存在， `hei=` 指定精確、最小或最大回應影像高度；請參閱 [符合=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md) 以取得詳細資訊。

如果 `scl=` 未指定，則會縮放複合影像以符合大小。 如果兩者 `wid=` 和 `hei=` 已指定，並且 `scl=` 未指定，則會縮放影像以完全符合wid/hei矩形，儘可能留下最小的背景區域顯示；在此情況下，影像會根據 `align=` 屬性。 背景區域已填滿 `bgc=`、或（若未透過指定） `attribute::BkgColor`.

>[!NOTE]
>
>如果計算的回覆影像大小大於 `attribute::MaxPix`.

## 屬性 {#section-534923644a1e464496eeba83dedcbd3c}

檢視屬性。 不論目前的圖層設定為何，皆會套用。

## 預設 {#section-76544d34806d4124a8b173e229cba71f}

如果兩者皆非 `wid=`， `hei=`、或 `scl=` 指定，回覆影像會具有複合影像的大小，或 `attribute::DefaultPix`，取較小者。

## 範例 {#section-eb10df7cd67e4733984810aaffd0b9e2}

要求影像以符合200x200矩形；如果影像不是正方形，則靠左上方對齊。 任何背景區域皆已填滿 `attribute::BkgColor`.

`http://server/myRootId/myImageId?wid=200&hei=200&align=-1,-1`

相同的影像，以200畫素的固定高度傳送，但具有符合影像外觀比例的可變寬度。 在此情況下，傳回的影像絕對不會有任何背景填滿區域。 請注意，在此案例中 `align=` 完全沒有效果。

`http://server/myRootId/myImageId?hei=200`

## 另請參閱 {#section-796e059e42ea4e86ab90ea3d024850ec}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ， [符合=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)， [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)， [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)， [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)， [rgn=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f)， [attribute：：DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)， [attribute：：MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
