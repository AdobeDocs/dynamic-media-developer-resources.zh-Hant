---
description: 最終視圖矩形。 允許將最終視圖影像拆分成若干條或多塊，這些條或多塊可以單獨傳送，由客戶無縫地重新組裝，而不會沿邊緣產生任何偽影。
solution: Experience Manager
title: 正確
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 1870001b-7904-470f-9582-984d453509ca
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 1%

---

# 正確{#rect}

最終視圖矩形。 允許將最終視圖影像拆分成若干條或多塊，這些條或多塊可以單獨傳送，由客戶無縫地重新組裝，而不會沿邊緣產生任何偽影。

`rect= *``*, *``*[, *`coordisescale`*]`

<table id="simpletable_69D112F85FA24EFCA727B398DC8ED699"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 坐標</span> </p> </td> 
  <td class="stentry"> <p>應用<span class="varname">縮放</span>後，從視圖影像的左上角到視圖矩形的左上角的像素偏移(int, int)，以像素表示。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 大小</span> </p></td> 
  <td class="stentry"> <p>ROI的大小（像素）（整、整）。 指定回覆影像大小。 在視圖影像未覆蓋的區域中，該影像被<span class="codeph"> bgc=</span>填充(如果請求中存在<span class="codeph"> fmt=*-alpha</span>，則為左透明)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> scale</span> </p></td> 
  <td class="stentry"> <p>比例因子（實數）。 小於1.0的值會降低解析度，而大於1.0的值會增加解析度。 </p></td> 
 </tr> 
</table>

使用此命令，影像伺服器可以通過HTTP傳送大型影像，否則，該HTTP將超過使用`attribute::MaxPix`配置的大小限制。

>[!NOTE]
>
>為了在使用JPEG壓縮時獲得最佳結果，條帶或拼貼大小應是JPEG編碼拼貼大小（16x16像素）的倍數。

## 範例 {#section-932fcfcb41d74a29bc929e4430c49601}

將可打印的CMYK影像分割成幾個全解析度條帶，以減小下載檔案的大小。 如果要求連續的影像：

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&fmt=tif&icc=WebCoated`

首先，獲取影像的相關資訊：

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&req=props`

文字回應包含下列屬性：

`image.width=2000 image.height=2400 image.version=37JK6NTvpvC42F5gOuLEVY`

根據這些資訊，我們決定要四塊600x2000像素條。 `rect=`命令用於描述條帶大小和位置。

由於此影像經常變更，因此我們將加入`id=`命令，以盡量降低從CDN或代理伺服器中快取的舊版影像中，出現一或多個片段的機率。 `image.version`屬性的值用於此目的。

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,0,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,600,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1200,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1800,2000,600`

## 屬性 {#section-aae223cee13e46d38b74680c048d945b}

檢視屬性。 無論目前的層設定為何，都適用。

在視圖影像外部延伸的ROI的任何區域都用`bgc=`補充。

重要`rect=`在&#x200B;*後應用*，並與`scl=`、`wid=`、`hei=`、`fit=`、`rgn=`和`align=`進行最終縮放和擬合。

## 預設 {#section-b296d3bbfb19441f87137a452b70f19a}

未修改的整個視圖影像(`rect=0,0,width,height,1.0`)。

## 請亦參閱 {#section-74015202c0c545ec82aec614d74b4bbd}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) ,  [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac),  [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47),  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7),  [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989),  [rgn=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f),  [屬性：:MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5),  [id=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0)
