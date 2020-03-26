---
description: 縮放檢視。 使用invFactor的反函式縮放合成影像。
seo-description: 縮放檢視。 使用invFactor的反函式縮放合成影像。
seo-title: scl
solution: Experience Manager
title: scl
topic: Scene7 Image Serving - Image Rendering API
uuid: 10a365dc-9fc1-4236-9528-4aca04a4ca19
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# scl{#scl}

縮放檢視。 使用invFactor的反函式縮放合成影像。

`scl= *`invFactor`*`

<table id="simpletable_A09F5EECAC2B4E0F8633D71C6AD36D8D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> invFactor</span> </p> </td> 
  <td class="stentry"> <p>反比例因子（實際大於0.0）。 </p></td> 
 </tr> 
</table>

No scaling is applied when `scl=1`. *`invFactor`* 大於1.0的縮放比和小於1.0的縮放比放大了複合影像。

如果 `scl=` 已指定， `wid=` 且和／或 `hei=` 也存在，則影像會裁切至縮放後 `wid=` 和／或 `hei=` 縮放。

>[!NOTE]
>
>如果計算或預設的回覆影像大小大於，則會傳回錯誤 `attribute::MaxPix`。

## 屬性 {#section-60af012719db477db4a4703e9a6da5f5}

檢視屬性。 不論目前的圖層設定如何，都適用。

## 預設 {#section-32502fa218a24e1f9c65f41c0260b56a}

如果未 `wid=`指 `hei=`定、 `scl=` 也未指定，則回覆影像將具有合成影像的大小，或 `attribute::DefaultPix`是較小的。

## 範例 {#section-a33f6239476a4b438d939656ad99aa76}

有關的常見應 [用程式](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) ，請參閱rotate=中的範例 `scl=`。

## 另請參閱 {#section-ccefd5de59924059903d66d4974ce317}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)，屬 [性：:DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
