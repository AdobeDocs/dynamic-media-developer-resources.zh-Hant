---
description: 查看背景顏色。 指定複合影像（視圖影像）的背景顏色。
solution: Experience Manager
title: BGC
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39ca0d63-55c6-40be-88b6-cf73828cc355
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 2%

---

# BGC{#bgc}

查看背景顏色。 指定複合影像（視圖影像）的背景顏色。

`bgc= *`color`*`

<table id="simpletable_998CF426296945FEA48D19E33B71A17E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 顏色</span></span> </p> </td> 
  <td class="stentry"> <p>灰色、RGB或CMYK顏色值。 </p></td> 
 </tr> 
</table>

指定用於視圖背景的不透明填充顏色。 僅當複合影像具有透明區域或複合影像具有與視圖矩形不同的長寬比時才可見。 如果忽略 `fmt=tif-alpha` 或 `fmt=png-alpha`或 `req=mask`。

>[!NOTE]
>
>「s」顏色尾碼被忽略 `bgc=`。 指定的顏色值 `bgc=` 始終與相應的輸出顏色空間相關聯。

## 屬性 {#section-b729b50b1ea7433b82ba34ecd61839cd}

查看屬性。 無論當前圖層設定如何都適用。 如果忽略 `req=mask`。 `fmt=tif-alpha`。 `fmt=png-alpha`。 `fmt=gif-alpha`或 `fmt=swf-alpha`。

忽略用顏色指定的任何Alpha值。

*`color`* 假定屬於輸出顏色空間(如 `icc=`)，並且應具有與輸出影像相同的像素類型。 如果像素類型不匹配， *`color`* 轉換。

## 預設 {#section-4e025cbd723547b5ab4450f7aad70da3}

`attribute::BkgColor`.

## 範例 {#section-7bcdfbc0e1274e86a69d39186b090789}

為縮略圖請求指定顯式背景顏色：

`http://server/myRootId/myImageId?req=tmb&bgc=214,245,130`

## 另請參閱 {#section-1e55f9f98f1847918a1725836a27cfaa}

[顏色](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93)。 [屬性：:BkgColor](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-bkgcolor.md#reference-ed53106ee50442d7a2dd3e1f60e6f0f8)。 [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)。 [請求=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)。 [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)。 [色彩管理](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
