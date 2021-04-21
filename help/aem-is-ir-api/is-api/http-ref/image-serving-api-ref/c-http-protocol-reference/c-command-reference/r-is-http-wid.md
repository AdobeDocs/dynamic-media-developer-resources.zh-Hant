---
description: 檢視寬度。 指定在請求中未顯示fit=時，回應影像（檢視影像）的寬度。
solution: Experience Manager
title: wid
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 3%

---


# wid{#wid}

檢視寬度。 指定在請求中未顯示fit=時，回應影像（檢視影像）的寬度。

` wid= *`val`*`

<table id="simpletable_E217453246F5441C896C1F69EA4D4218"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>影像寬度（以像素為單位）（整數大於0）。 </p> </td> 
 </tr> 
</table>

如果同時指定`hei=`和`scl=`，則可根據`align=`屬性裁切合成影像。 當`fit=`出現時，`wid=`會指定精確、最小或最大回應影像寬度；如需詳細資訊，請參閱`fit=`的說明。

如果未指定`scl=`，則複合影像會縮放以適合。 如果同時指定`wid=`和`hei=`，且未指定`scl=`，則影像會縮放以完全符合寬／黑矩形，留下盡可能少的背景區域。 在這種情況下，影像會根據`align=`屬性放在檢視矩形內。

>[!NOTE]
>
>如果計算或預設回覆影像大小大於`attribute::MaxPix`，則會傳回錯誤。

## 預設 {#section-976d4c8554a34c899f85d172f6ac6f58}

如果未指定`wid=`、`hei=`和`scl=`，則回覆影像的大小為複合影像或`attribute::DefaultPix`，以較小者為準。

## 屬性 {#section-c93b7ce1b0d2475f80b06264b45d1285}

檢視屬性。 不論目前的圖層設定為何，都適用。

## 範例 {#section-82bc98b7c15a451bbe9b915d414c0470}

請求影像以符合200x200矩形；如果影像不是正方形，則右上對齊影像。 任何背景區域都會填入`attribute::BkgColor`。

` http:// *`伺服器`*/myRootId/myImageId?wid=200&hei=200&align=1,-1`

相同的影像以固定寬度200像素傳送，但高度可變，以維持影像的高寬比。 在這種情況下，傳回的影像從未有任何背景填滿區域。 請注意，在此情況下， align=將完全無效。

` http:// *`伺服器`*/myRootId/myImageId?wid=200`

## 另請參閱 {#section-4e9659238d6545498378ca8b1f3ec4ae}

[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96) , fit= [, scl=align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)align= [, ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7) [](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1) [Pix屬性：Pix:DefaultPix屬性：:MaxMaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
