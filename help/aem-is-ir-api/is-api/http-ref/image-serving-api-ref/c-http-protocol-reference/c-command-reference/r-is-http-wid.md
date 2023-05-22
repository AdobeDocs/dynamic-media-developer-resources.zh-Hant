---
description: 視圖寬度。 指定請求中不存在fit=時響應影像（視圖影像）的寬度。
solution: Experience Manager
title: wid
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ba22c79b-da59-4993-aa1c-2c990a0c4be5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 2%

---

# wid{#wid}

視圖寬度。 指定請求中不存在fit=時響應影像（視圖影像）的寬度。

` wid= *`谷`*`

<table id="simpletable_E217453246F5441C896C1F69EA4D4218"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 谷 </span> </p> </td> 
  <td class="stentry"> <p>影像寬度（以像素為單位）（大於0的整數）。 </p> </td> 
 </tr> 
</table>

如果兩者都 `hei=` 和 `scl=` 指定，可根據 `align=` 屬性。 當 `fit=` 現在， `wid=` 指定精確、最小或最大響應影像寬度；請參閱 `fit=` 的雙曲餘切值。

如果 `scl=` 未指定，將縮放複合影像以適合。 如果兩者都 `wid=` 和 `hei=` 已指定 `scl=` 未指定，則縮放影像以完全適合在wid/hei矩形中，使盡可能少的背景區域暴露。 在這種情況下，根據 `align=` 屬性。

>[!NOTE]
>
>如果計算的或預設的答復影像大小大於 `attribute::MaxPix`。

## 預設 {#section-976d4c8554a34c899f85d172f6ac6f58}

如果兩者都不 `wid=`。 `hei=`，或 `scl=` 已指定，回復影像將具有複合影像的大小，或 `attribute::DefaultPix`，以較小者為準。

## 屬性 {#section-c93b7ce1b0d2475f80b06264b45d1285}

查看屬性。 無論當前圖層設定如何都適用。

## 範例 {#section-82bc98b7c15a451bbe9b915d414c0470}

請求將影像放入200x200矩形；如果影像不是正方形，則右上對齊。 任何背景區域都填充 `attribute::BkgColor`。

` http:// *`伺服器`*/myRootId/myImageId?wid=200&hei=200&align=1,-1`

以200像素的固定寬度傳送的相同影像，但具有可變高度以保持影像的縱橫比。 在這種情況下，返回的影像從來沒有任何背景填充區域。 請注意，在這種情況下， align=將不會產生任何效果。

` http:// *`伺服器`*/myRootId/myImageId?wid=200`

## 另請參閱 {#section-4e9659238d6545498378ca8b1f3ec4ae}

[黑=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96) 。 [合適=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)。 [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)。 [對齊=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)。 [屬性：:DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)。 [屬性：:MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
