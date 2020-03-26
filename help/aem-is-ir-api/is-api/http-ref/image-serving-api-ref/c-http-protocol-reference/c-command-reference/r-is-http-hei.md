---
description: 檢視高度. 指定在請求中未顯示符合時的回應影像（檢視影像）高度。
seo-description: 檢視高度. 指定在請求中未顯示符合時的回應影像（檢視影像）高度。
seo-title: hei
solution: Experience Manager
title: hei
topic: Scene7 Image Serving - Image Rendering API
uuid: 307952bb-604f-49b4-bce3-b7a7fc7ec63b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# hei{#hei}

檢視高度. 指定在請求中未顯示符合時的回應影像（檢視影像）高度。

` hei= *`val`*`

<table id="simpletable_1A36827B6E6647888A4E6E868975D716"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span></span> </p> </td> 
  <td class="stentry"> <p>影像高度（以像素為單位，整數大於0）。 </p> </td> 
 </tr> 
</table>

如果同時 `wid=` 指 `scl=` 定和，則可根據屬性裁切合成 `align=`影像。 出現 `fit=` 時，請指 `hei=` 定精確、最小或最大響應影像高度；有關詳細資訊，請參 ` [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)` 閱的說明。

如果未 `scl=` 指定，則複合影像會縮放以適合。 如果同時 `wid=` 指定和 `hei=` 未指定，則 `scl=` 會縮放影像以完全配合寬／高矩形，使盡可能少的背景區域暴露；在這種情況下，影像會根據屬性放在檢視矩形內 `align=` 。 背景區域會填入 `bgc=`或（若未指定） `attribute::BkgColor`。

>[!NOTE]
>
>如果計算的回覆影像大小大於，則會傳回錯誤 `attribute::MaxPix`。

## 屬性 {#section-534923644a1e464496eeba83dedcbd3c}

檢視屬性。 不論目前的圖層設定為何，都適用。

## 預設 {#section-76544d34806d4124a8b173e229cba71f}

如果未 `wid=`指 `hei=`定、 `scl=` 也未指定，則回覆影像具有複合影像的大小，或 `attribute::DefaultPix`者，以較小者為準。

## 範例 {#section-eb10df7cd67e4733984810aaffd0b9e2}

請求影像以符合200x200矩形；如果影像不是正方形，則左上對齊影像。 任何背景區域都會填入 `attribute::BkgColor`。

`http://server/myRootId/myImageId?wid=200&hei=200&align=-1,-1`

相同的影像以200像素的固定高度傳送，但寬度可變以符合影像的寬高比。 在這種情況下，傳回的影像從未有任何背景填滿區域。 請注意，在此情 `align=` 況下，完全沒有作用。

`http://server/myRootId/myImageId?hei=200`

## 另請參閱 {#section-796e059e42ea4e86ab90ea3d024850ec}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [scl==align](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)align, [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)[rgn=rgn=fit=，符合為，符合為Pix Fit屬性：DefaultPixDefaultMaditPix:DowntMaxPixParit屬性：::MaxPixPixPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
