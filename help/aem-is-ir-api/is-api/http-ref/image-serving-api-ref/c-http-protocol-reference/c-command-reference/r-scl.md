---
description: 縮放視圖。 按invFactor的逆值縮放複合影像。
solution: Experience Manager
title: scl
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 297d187c-3a52-45ff-b73d-0b0e4b956080
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 4%

---

# scl{#scl}

縮放視圖。 按invFactor的逆值縮放複合影像。

`scl= *`inv系數`*`

<table id="simpletable_A09F5EECAC2B4E0F8633D71C6AD36D8D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> inv系數</span> </p> </td> 
  <td class="stentry"> <p>反比例因子（實數大於0.0）。 </p></td> 
 </tr> 
</table>

在 `scl=1`。 *`invFactor`* 大於1.0的下縮放和小於1.0的放大了複合影像。

如果 `scl=` 已指定，並且 `wid=` 和/或 `hei=` 也存在，影像被裁剪到 `wid=` 和/或 `hei=` 縮放後。

>[!NOTE]
>
>如果計算的或預設的答復影像大小大於 `attribute::MaxPix`。

## 屬性 {#section-60af012719db477db4a4703e9a6da5f5}

查看屬性。 應用，與當前圖層設定無關。

## 預設 {#section-32502fa218a24e1f9c65f41c0260b56a}

如果兩者都不 `wid=`。 `hei=`，或 `scl=` 已指定，回復影像將具有複合影像的大小，或 `attribute::DefaultPix`，以較小者為準。

## 範例 {#section-a33f6239476a4b438d939656ad99aa76}

請參閱中的示例 [旋轉=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) 用於 `scl=`。

## 另請參閱 {#section-ccefd5de59924059903d66d4974ce317}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) 。 [黑=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)。 [屬性：:DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
