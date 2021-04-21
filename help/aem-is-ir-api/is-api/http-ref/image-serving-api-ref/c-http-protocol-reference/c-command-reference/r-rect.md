---
description: 最終檢視矩形。 允許最終視圖影像分解成若干條或拼貼，這些條或拼貼可以單獨傳送，並由客戶無縫地重新組裝，而沿邊緣沒有不自然現象。
solution: Experience Manager
title: rect
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 1%

---


# rect{#rect}

最終檢視矩形。 允許最終視圖影像分解成若干條或拼貼，這些條或拼貼可以單獨傳送，並由客戶無縫地重新組裝，而沿邊緣沒有不自然現象。

`rect= *``*, *``*[, *`Coordsiscale`*]`

<table id="simpletable_69D112F85FA24EFCA727B398DC8ED699"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 坐標</span> </p> </td> 
  <td class="stentry"> <p>在套用<span class="varname">縮放</span>後，從檢視影像的左上角到檢視矩形的左上角的像素偏移(int, int)，以像素表示。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 大小</span> </p></td> 
  <td class="stentry"> <p>ROI的大小（以像素為單位，int、int）。 指定回覆影像大小。 在視圖影像未覆蓋的區域(或者，如果請求中存在<span class="codeph"> fmt=*-alpha↑[a3/]，則用<span class="codeph"> bgc=</span>填充影像。</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> scale</span> </p></td> 
  <td class="stentry"> <p>比例系數（實數）。 小於1.0的值會降低解析度，而大於1.0的值則會提高解析度。 </p></td> 
 </tr> 
</table>

使用此命令，影像伺服可透過HTTP傳送大型影像，否則會超過使用`attribute::MaxPix`設定的大小限制。

>[!NOTE]
>
>為獲得使用JPEG壓縮時的最佳結果，條帶或拼貼大小應是JPEG編碼拼貼大小（16x16像素）的倍數。

## 範例 {#section-932fcfcb41d74a29bc929e4430c49601}

將可列印的CMYK影像分割成數個完整解析度的色帶，以減少下載檔案的大小。 如果我們要請求連續的影像：

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&fmt=tif&icc=WebCoated`

首先，獲得影像的相關資訊：

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&req=props`

文字回應包含下列屬性：

`image.width=2000 image.height=2400 image.version=37JK6NTvpvC42F5gOuLEVY`

根據這些資訊，我們決定要4個600x2000像素條。 `rect=`命令用於描述條帶大小和位置。

由於此影像經常變更，因此我們將加入`id=`命令，以盡量降低從舊版影像快取至CDN或Proxy伺服器中的一或多個片段時，發生錯誤的機率。 `image.version`屬性的值用於此用途。

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,0,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,600,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1200,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1800,2000,600`

## 屬性 {#section-aae223cee13e46d38b74680c048d945b}

檢視屬性。 不論目前的圖層設定為何，都適用。

ROI延伸至檢視影像以外的任何區域都會填入`bgc=`。

重要提示：`rect=`在&#x200B;*最終縮放和與`scl=`、`wid=`、`hei=`、`fit=`、`rgn=`和`align=`配合後套用*。

## 預設 {#section-b296d3bbfb19441f87137a452b70f19a}

完整、未修改的檢視影像(`rect=0,0,width,height,1.0`)。

## 請亦參閱 {#section-74015202c0c545ec82aec614d74b4bbd}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , extend= [, hei=, ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)li= [, scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47)align,gn pix=lign,  [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f) [](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5) [pix aglin=throb, Attribute:MaxMax:chrobod=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0)
