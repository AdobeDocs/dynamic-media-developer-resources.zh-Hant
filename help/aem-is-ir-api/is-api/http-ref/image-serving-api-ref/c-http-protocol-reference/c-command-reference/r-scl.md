---
title: scl
description: 縮放檢視。 依照invFactor的逆比例縮放複合影像。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 297d187c-3a52-45ff-b73d-0b0e4b956080
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 2%

---

# scl{#scl}

縮放檢視。 依照invFactor的逆比例縮放複合影像。

`scl= *`invFactor`*`

<table id="simpletable_A09F5EECAC2B4E0F8633D71C6AD36D8D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> invFactor</span> </p> </td> 
  <td class="stentry"> <p>反比例因子（實數大於0.0）。 </p></td> 
 </tr> 
</table>

`scl=1`時未套用任何縮放。 大於1.0的&#x200B;*`invFactor`*&#x200B;值會放大複合影像，但小於1.0。

若已指定`scl=`，並且也有`wid=`和/或`hei=`，則縮放後影像會裁切為`wid=`和/或`hei=`。

>[!NOTE]
>
>如果計算的或預設的回覆影像大小大於`attribute::MaxPix`，則會傳回錯誤。

## 屬性 {#section-60af012719db477db4a4703e9a6da5f5}

檢視屬性。 無論目前的圖層設定為何，都適用。

## 預設 {#section-32502fa218a24e1f9c65f41c0260b56a}

若未指定`wid=`、`hei=`或`scl=`，則回覆影像的大小可能為複合影像或`attribute::DefaultPix` （取較小者）。

## 範例 {#section-a33f6239476a4b438d939656ad99aa76}

如需常見的`scl=`應用程式，請參閱[rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096)中的範例。

## 另請參閱 {#section-ccefd5de59924059903d66d4974ce317}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ， [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)， [attribute：：DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
