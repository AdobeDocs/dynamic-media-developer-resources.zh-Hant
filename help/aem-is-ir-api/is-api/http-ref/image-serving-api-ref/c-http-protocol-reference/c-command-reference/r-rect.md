---
description: 最終視圖矩形。 允許將最終視圖影像分解成若干條帶或磁貼，這些條帶或磁貼可由客戶端獨立傳送和無縫地重新組裝，而不會沿邊緣產生任何偽影。
solution: Experience Manager
title: 正
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1870001b-7904-470f-9582-984d453509ca
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 1%

---

# 正{#rect}

最終視圖矩形。 允許將最終視圖影像分解成若干條帶或磁貼，這些條帶或磁貼可由客戶端獨立傳送和無縫地重新組裝，而不會沿邊緣產生任何偽影。

`rect= *`坐標`*, *`大小`*[, *`規模`*]`

<table id="simpletable_69D112F85FA24EFCA727B398DC8ED699"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 坐標</span> </p> </td> 
  <td class="stentry"> <p>從視圖影像左上角到視圖矩形(int, int)左上角的像素偏移，以像素表示，在 <span class="varname"> 規模</span> 的子菜單。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 大小</span> </p></td> 
  <td class="stentry"> <p>ROI的大小（以像素為單位）(int、int)。 指定回復影像大小。 影像已填充 <span class="codeph"> bgc=</span> 在視圖影像未覆蓋的區域(或左側透明，如果 <span class="codeph"> fmt=*-α</span> 在請求中出現)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> scale</span> </p></td> 
  <td class="stentry"> <p>比例因子（實數）。 小於1.0的值會降低解析度，大於1.0的值會提高解析度。 </p></td> 
 </tr> 
</table>

使用此命令，影像服務可以通過HTTP傳送大型影像，否則這些影像將超過配置為的大小限制 `attribute::MaxPix`。

>[!NOTE]
>
>為了在使用JPEG壓縮時獲得最佳結果，條帶或磁貼大小應是JPEG編碼磁貼大小（16x16像素）的倍數。

## 範例 {#section-932fcfcb41d74a29bc929e4430c49601}

將可打印的CMYK影像分割成若干全解析度條，以減小下載檔案大小。 如果要請求連續影像：

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&fmt=tif&icc=WebCoated`

首先，獲取影像的相關資訊：

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&req=props`

文本響應包括以下屬性：

`image.width=2000 image.height=2400 image.version=37JK6NTvpvC42F5gOuLEVY`

根據這些資訊，我們決定要4個600x2000像素條。 的 `rect=` 命令用於描述條帶大小和位置。

由於此影像經常更改，因此我們將 `id=` 命令，以最小化我們最終從舊版本映像中執行一個或多個剝離操作的可能性，這些映像可能已快取到CDN或代理伺服器中。 的值 `image.version` 屬性用於此目的。

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,0,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,600,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1200,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1800,2000,600`

## 屬性 {#section-aae223cee13e46d38b74680c048d945b}

查看屬性。 無論當前圖層設定如何都適用。

擴展到視圖影像外的ROI的任何區域都用填充 `bgc=`。

重要 `rect=` 已應用 *後* 最終縮放和擬合 `scl=`。 `wid=`。 `hei=`。 `fit=`。 `rgn=`, `align=`。

## 預設 {#section-b296d3bbfb19441f87137a452b70f19a}

完整、未修改的視圖影像( `rect=0,0,width,height,1.0`)。

## 請亦參閱 {#section-74015202c0c545ec82aec614d74b4bbd}

[作物=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) 。 [擴展=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)。 [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47)。 [黑=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)。 [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)。 [對齊=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)。 [合適=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)。 [rgn=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f)。 [屬性：:MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)。 [id=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0)
