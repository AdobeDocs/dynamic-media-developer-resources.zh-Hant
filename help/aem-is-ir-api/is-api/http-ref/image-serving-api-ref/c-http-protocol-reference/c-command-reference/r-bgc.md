---
title: bgc
description: 檢視背景顏色。 指定複合影像（檢視影像）的背景色彩。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39ca0d63-55c6-40be-88b6-cf73828cc355
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 2%

---

# bgc{#bgc}

檢視背景顏色。 指定複合影像（檢視影像）的背景色彩。

`bgc= *`color`*`

<table id="simpletable_998CF426296945FEA48D19E33B71A17E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">色彩</span></span> </p> </td> 
  <td class="stentry"> <p>灰色、RGB或CMYK色彩值。 </p></td> 
 </tr> 
</table>

指定要用於檢視背景的不透明填色色彩。 僅當複合影像具有透明區域，或複合影像的外觀比例與檢視矩形不同時，才可見。 已忽略`fmt=tif-alpha`、`fmt=png-alpha`或`req=mask`。

>[!NOTE]
>
>`bgc=`已忽略&#39;s&#39;色彩尾碼。 以`bgc=`指定的色彩值一律與各自的輸出色域相關聯。

## 屬性 {#section-b729b50b1ea7433b82ba34ecd61839cd}

檢視屬性。 不論目前的圖層設定為何，皆會套用。 已忽略`req=mask`、`fmt=tif-alpha`、`fmt=png-alpha`、`fmt=gif-alpha`或`fmt=swf-alpha`。

會忽略以顏色指定的任何Alpha值。

假設&#x200B;*`color`*&#x200B;屬於輸出色域（如`icc=`所指定），而且應該與輸出影像有相同的畫素型別。 如果畫素型別不符，則會使用天真的轉換來轉換&#x200B;*`color`*。

## 預設 {#section-4e025cbd723547b5ab4450f7aad70da3}

`attribute::BkgColor`.

## 範例 {#section-7bcdfbc0e1274e86a69d39186b090789}

指定縮圖要求的明確背景顏色：

`http://server/myRootId/myImageId?req=tmb&bgc=214,245,130`

## 另請參閱 {#section-1e55f9f98f1847918a1725836a27cfaa}

[色彩](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93)，[屬性：：BkgColor](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-bkgcolor.md#reference-ed53106ee50442d7a2dd3e1f60e6f0f8)，[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)，[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)，[icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)，[色彩管理](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
