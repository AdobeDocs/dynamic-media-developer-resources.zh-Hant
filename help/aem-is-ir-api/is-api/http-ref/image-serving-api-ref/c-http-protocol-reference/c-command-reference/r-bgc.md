---
description: 檢視背景顏色。 指定複合影像（視圖影像）的背景顏色。
solution: Experience Manager
title: bgc
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 3%

---


# bgc{#bgc}

檢視背景顏色。 指定複合影像（視圖影像）的背景顏色。

`bgc= *`color`*`

<table id="simpletable_998CF426296945FEA48D19E33B71A17E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 顏色</span></span> </p> </td> 
  <td class="stentry"> <p>灰色、RGB或CMYK顏色值。 </p></td> 
 </tr> 
</table>

指定用於視圖背景的不透明填充顏色。 僅當複合影像具有透明區域或複合影像具有與視圖矩形不同的外觀比例時才可見。 如果`fmt=tif-alpha`或`fmt=png-alpha`或`req=mask`，則忽略。

>[!NOTE]
>
>`bgc=`會忽略&#39;s&#39;色彩字尾。 使用`bgc=`指定的顏色值始終與各自的輸出顏色空間相關聯。

## 屬性 {#section-b729b50b1ea7433b82ba34ecd61839cd}

檢視屬性。 不論目前的圖層設定為何，都適用。 如果`req=mask`、`fmt=tif-alpha`、`fmt=png-alpha`、`fmt=gif-alpha`或`fmt=swf-alpha`，則忽略。

任何以顏色指定的alpha值都會被忽略。

*`color`* 假設屬於輸出色域(如指定 `icc=`)，且像素類型應與輸出影像相同。如果像素類型不匹配，則使用天真的轉換來轉換&#x200B;*`color`*。

## 預設 {#section-4e025cbd723547b5ab4450f7aad70da3}

`attribute::BkgColor`.

## 範例 {#section-7bcdfbc0e1274e86a69d39186b090789}

指定縮圖要求的明確背景顏色：

`http://server/myRootId/myImageId?req=tmb&bgc=214,245,130`

## 另請參閱 {#section-1e55f9f98f1847918a1725836a27cfaa}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93), attribute::BkgColor [, fmt=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-bkgcolor.md#reference-ed53106ee50442d7a2dd3e1f60e6f0f8)req= [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)req,  [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517) [color Management，色彩管理](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
