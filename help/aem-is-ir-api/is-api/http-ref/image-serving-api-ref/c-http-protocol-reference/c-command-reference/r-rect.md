---
title: 矩形
description: 最終檢視矩形。 可將最終檢視影像拆解成數個片段或圖磚，這些片段或圖磚可由使用者端分別傳送並順暢地重新組裝，邊緣不會出現任何不自然感。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1870001b-7904-470f-9582-984d453509ca
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 1%

---

# 矩形{#rect}

最終檢視矩形。 可將最終檢視影像拆解成數個片段或圖磚，這些片段或圖磚可由使用者端分別傳送並順暢地重新組裝，邊緣不會出現任何不自然感。

`rect= *`座標`*, *`大小`*[, *`縮放`*]`

<table id="simpletable_69D112F85FA24EFCA727B398DC8ED699"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 座標</span> </p> </td> 
  <td class="stentry"> <p>從檢視影像左上角到檢視矩形(int， int)左上角的畫素位移（以畫素表示），在後方 <span class="varname"> 縮放</span> 中所有規則的URL區段。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 大小</span> </p></td> 
  <td class="stentry"> <p>ROI的大小（畫素，int， int）。 指定回覆影像大小。 影像已填滿 <span class="codeph"> bgc=</span> 在檢視影像未覆蓋的區域中(或左方透明，如果 <span class="codeph"> fmt=*-alpha</span> （會出現在請求中）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> scale</span> </p></td> 
  <td class="stentry"> <p>縮放因數（實數）。 小於1.0的值會降低解析度，大於1.0的值則會增加解析度。 </p></td> 
 </tr> 
</table>

使用此命令，「影像伺服」可以透過HTTP傳送大型影像，否則會超過設定的大小限制。 `attribute::MaxPix`.

>[!NOTE]
>
>為達到使用JPEG壓縮時的最佳效果，條紋或並排大小應為JPEG編碼並排大小（16x16畫素）的倍數。

## 範例 {#section-932fcfcb41d74a29bc929e4430c49601}

將可列印的CMYK影像分割成數個完整解析度的色條，以減少下載檔案的大小。 如果我們要請求連續的影像：

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&fmt=tif&icc=WebCoated`

首先，取得影像的相關資訊：

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&req=props`

文字回應包含下列屬性：

`image.width=2000 image.height=2400 image.version=37JK6NTvpvC42F5gOuLEVY`

根據此資訊，我們決定想要四條600x2000畫素的色條。 此 `rect=` 指令用於描述分段大小和位置。

由於此影像經常變更，因此我們將包含 `id=` 將舊版影像中可能已在CDN或Proxy伺服器中快取的一或多個片段最後出現的機率降到最低。 的值 `image.version` 屬性會用於此目的。

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,0,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,600,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1200,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1800,2000,600`

## 屬性 {#section-aae223cee13e46d38b74680c048d945b}

檢視屬性。 不論目前的圖層設定為何，皆會套用。

任何延伸至檢視影像外部的ROI區域皆會填入 `bgc=`.

重要 `rect=` 已套用 *晚於* 最終縮放與彎管頭 `scl=`， `wid=`， `hei=`， `fit=`， `rgn=`、和 `align=`.

## 預設 {#section-b296d3bbfb19441f87137a452b70f19a}

完整、未修改的檢視影像( `rect=0,0,width,height,1.0`)。

## 請亦參閱 {#section-74015202c0c545ec82aec614d74b4bbd}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) ， [延伸=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)， [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47)， [嘻=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)， [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)， [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)， [符合=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)， [rgn=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f)， [attribute：：MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)， [id=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0)
