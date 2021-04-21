---
description: 檢視高度. 指定在請求中未顯示符合時的回應影像（檢視影像）高度。
solution: Experience Manager
title: hei
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 3%

---


# hei{#hei}

檢視高度. 指定在請求中未顯示符合時的回應影像（檢視影像）高度。

` hei= *`val`*`

<table id="simpletable_1A36827B6E6647888A4E6E868975D716"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var  </span> </span> </p> </td> 
  <td class="stentry"> <p>影像高度（以像素為單位，整數大於0）。 </p> </td> 
 </tr> 
</table>

如果同時指定`wid=`和`scl=`，則可根據`align=`屬性裁切合成影像。 當`fit=`出現時，`hei=`會指定精確、最小或最大的回應影像高度；如需詳細資訊，請參閱` [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)`的說明。

如果未指定`scl=`，則複合影像會縮放以適合。 如果同時指定`wid=`和`hei=`，且未指定`scl=`，則影像會縮放以完全符合寬／黑矩形，留下盡可能少的背景區域；在這種情況下，影像會根據`align=`屬性放在檢視矩形內。 背景區域填入`bgc=`，若未以`attribute::BkgColor`指定則填入。

>[!NOTE]
>
>如果計算的回覆影像大小大於`attribute::MaxPix`，則會傳回錯誤。

## 屬性 {#section-534923644a1e464496eeba83dedcbd3c}

檢視屬性。 不論目前的圖層設定為何，都適用。

## 預設 {#section-76544d34806d4124a8b173e229cba71f}

如果未指定`wid=`、`hei=`和`scl=`，則回復影像具有複合影像的大小或`attribute::DefaultPix`（以較小者為準）。

## 範例 {#section-eb10df7cd67e4733984810aaffd0b9e2}

請求影像以符合200x200矩形；如果影像不是正方形，則左上對齊影像。 任何背景區域都會填入`attribute::BkgColor`。

`http://server/myRootId/myImageId?wid=200&hei=200&align=-1,-1`

相同的影像以200像素的固定高度傳送，但寬度可變以符合影像的寬高比。 在這種情況下，傳回的影像從未有任何背景填滿區域。 請注意，在此情況下，`align=`將完全無效。

`http://server/myRootId/myImageId?hei=200`

## 另請參閱 {#section-796e059e42ea4e86ab90ea3d024850ec}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [scl==align](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7),  [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), rgn=fit=,符合 [fit，符合為Pix屬性：DefaultPixDefaultMaxPix:DamaxPixPixPixPixPidid屬性](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f)wid=wid=wid=wid=witWid=wid=wid=wid=wid=wid=wit=wid=wid=wid=wid=wid=wit=wid=witititit=wid=wid=wid=wid=wid=wititititid=wititititid=witid=witid=wit= [,](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1), [, ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
