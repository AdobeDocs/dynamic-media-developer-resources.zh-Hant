---
description: 檢視背景顏色。 指定複合影像（視圖影像）的背景顏色。
solution: Experience Manager
title: bgc
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39ca0d63-55c6-40be-88b6-cf73828cc355
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 3%

---

# bgc{#bgc}

檢視背景顏色。 指定複合影像（視圖影像）的背景顏色。

`bgc= *`color`*`

<table id="simpletable_998CF426296945FEA48D19E33B71A17E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 色彩</span></span> </p> </td> 
  <td class="stentry"> <p>灰色、RGB或CMYK顏色值。 </p></td> 
 </tr> 
</table>

指定用於視圖背景的不透明填充顏色。 僅當複合影像具有透明區域，或複合影像具有與視圖矩形不同的外觀比例時才可見。 若`fmt=tif-alpha`或`fmt=png-alpha`或`req=mask`，則忽略。

>[!NOTE]
>
>`bgc=`會忽略「s」顏色尾碼。 使用`bgc=`指定的顏色值始終與相應的輸出顏色空間相關聯。

## 屬性 {#section-b729b50b1ea7433b82ba34ecd61839cd}

檢視屬性。 無論目前的層設定為何，都適用。 若`req=mask`、`fmt=tif-alpha`、`fmt=png-alpha`、`fmt=gif-alpha`或`fmt=swf-alpha`，則忽略。

任何以顏色指定的Alpha值都會被忽略。

*`color`* 假設屬於輸出顏色空間(如指定 `icc=`)，且像素類型應與輸出影像相同。如果像素類型不匹配，則使用天真轉換來轉換&#x200B;*`color`*。

## 預設 {#section-4e025cbd723547b5ab4450f7aad70da3}

`attribute::BkgColor`.

## 範例 {#section-7bcdfbc0e1274e86a69d39186b090789}

為縮圖請求指定明確的背景顏色：

`http://server/myRootId/myImageId?req=tmb&bgc=214,245,130`

## 另請參閱 {#section-1e55f9f98f1847918a1725836a27cfaa}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93),  [attribute::BkgColor](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-bkgcolor.md#reference-ed53106ee50442d7a2dd3e1f60e6f0f8),  [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a),  [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76),  [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517),  [色彩管理](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
