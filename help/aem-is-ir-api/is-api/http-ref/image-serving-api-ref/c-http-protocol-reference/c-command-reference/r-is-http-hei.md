---
description: 檢視高度. 指定請求中不存在適合時的響應影像（視圖影像）的高度。
solution: Experience Manager
title: hei
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c812c7f0-4ac1-42cb-be47-7baebd8caf60
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 平{#hei}

檢視高度. 指定請求中不存在適合時的響應影像（視圖影像）的高度。

` hei= *`谷`*`

<table id="simpletable_1A36827B6E6647888A4E6E868975D716"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>影像高度（以像素為單位）（大於0的整數）。 </p> </td> 
 </tr> 
</table>

如果兩者都 `wid=` 和 `scl=` 指定，可根據 `align=`屬性。 當 `fit=` 現在， `hei=` 指定精確、最小或最大響應影像高度；請參閱 [合適=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md) 的雙曲餘切值。

如果 `scl=` 未指定，將縮放複合影像以適合。 如果兩者都 `wid=` 和 `hei=` 已指定 `scl=` 未指定，則縮放影像以完全適合寬/黑矩形，使盡可能少的背景區域暴露；在這種情況下，影像會根據 `align=` 屬性。 背景區域填充了 `bgc=`，或，如果未指定 `attribute::BkgColor`。

>[!NOTE]
>
>如果計算的答復影像大小大於 `attribute::MaxPix`。

## 屬性 {#section-534923644a1e464496eeba83dedcbd3c}

查看屬性。 無論當前圖層設定如何都適用。

## 預設 {#section-76544d34806d4124a8b173e229cba71f}

如果兩者都不 `wid=`。 `hei=`，或 `scl=` 已指定，回復影像的大小或 `attribute::DefaultPix`，以較小者為準。

## 範例 {#section-eb10df7cd67e4733984810aaffd0b9e2}

請求將影像放入200x200矩形；如果影像不是正方形，則左上對齊。 任何背景區域都填充 `attribute::BkgColor`。

`http://server/myRootId/myImageId?wid=200&hei=200&align=-1,-1`

相同的影像，以200像素的固定高度傳送，但具有與影像的縱橫比匹配的可變寬度。 在這種情況下，返回的影像從來沒有任何背景填充區域。 請注意，在本例中 `align=` 根本沒有效果。

`http://server/myRootId/myImageId?hei=200`

## 另請參閱 {#section-796e059e42ea4e86ab90ea3d024850ec}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) 。 [合適=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)。 [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)。 [對齊=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)。 [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)。 [rgn=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f)。 [屬性：:DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)。 [屬性：:MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
