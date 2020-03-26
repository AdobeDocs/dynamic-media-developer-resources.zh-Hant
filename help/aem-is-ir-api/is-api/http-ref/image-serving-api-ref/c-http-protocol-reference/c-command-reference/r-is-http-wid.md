---
description: 檢視寬度。 指定在請求中未顯示fit=時，回應影像（檢視影像）的寬度。
seo-description: 檢視寬度。 指定在請求中未顯示fit=時，回應影像（檢視影像）的寬度。
seo-title: wid
solution: Experience Manager
title: wid
topic: Scene7 Image Serving - Image Rendering API
uuid: 30aeeea0-c8c9-40b9-a244-2802a7102dd6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# wid{#wid}

檢視寬度。 指定在請求中未顯示fit=時，回應影像（檢視影像）的寬度。

` wid= *`val`*`

<table id="simpletable_E217453246F5441C896C1F69EA4D4218"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>影像寬度（以像素為單位）（整數大於0）。 </p> </td> 
 </tr> 
</table>

如果同時 `hei=` 指定 `scl=` 和，則可根據屬性裁切合成影 `align=` 像。 出現 `fit=` 時，請指 `wid=` 定精確、最小或最大響應影像寬度；有關詳細資訊，請參 `fit=` 閱的說明。

如果未 `scl=` 指定，則複合影像會縮放以適合。 如果同 `wid=` 時指 `hei=` 定和未指定， `scl=` 則影像會縮放以完全符合寬／高矩形，留下盡可能少的背景區域。 在這種情況下，影像會根據屬性放在檢視矩形內 `align=` 。

>[!NOTE]
>
>如果計算或預設的回覆影像大小大於，則會傳回錯誤 `attribute::MaxPix`。

## 預設 {#section-976d4c8554a34c899f85d172f6ac6f58}

如果未 `wid=`指 `hei=`定、 `scl=` 也未指定，則回覆影像將具有合成影像的大小，或 `attribute::DefaultPix`是較小的。

## 屬性 {#section-c93b7ce1b0d2475f80b06264b45d1285}

檢視屬性。 不論目前的圖層設定為何，都適用。

## 範例 {#section-82bc98b7c15a451bbe9b915d414c0470}

請求影像以符合200x200矩形；如果影像不是正方形，則右上對齊影像。 任何背景區域都會填入 `attribute::BkgColor`。

` http:// *`伺服器`*/myRootId/myImageId?wid=200&hei=200&align=1,-1`

相同的影像以固定寬度200像素傳送，但高度可變，以維持影像的高寬比。 在這種情況下，傳回的影像從未有任何背景填滿區域。 請注意，在此情況下， align=將完全無效。

` http:// *`伺服器`*/myRootId/myImageId?wid=200`

## 另請參閱 {#section-4e9659238d6545498378ca8b1f3ec4ae}

[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96) , fit= [, scl=align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)[, Pix屬性：Pix:DefaultPix屬性：:MaxMaxPix屬性](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
