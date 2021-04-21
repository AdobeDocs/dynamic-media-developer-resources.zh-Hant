---
description: Jpeg大小（以千位元組為單位）。 指定JPEG回應的最大大小（以千位元組為單位）。
solution: Experience Manager
title: jpegSize
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 4%

---


# jpegSize{#jpegsize}

Jpeg大小（以千位元組為單位）。 指定JPEG回應的最大大小（以千位元組為單位）。

`jpegSize= *`大小`*`

<table id="simpletable_EC2A8D8B65854B45B9CB184DA1069355"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 大小</span></span> </p> </td> 
  <td class="stentry"> <p>大小（千位元組）。 </p></td> 
 </tr> 
</table>

如果此值設為正值，且具有指定JPEG品質的JPEG回應未超過此值，則會傳回該影像作為回應。 否則，JPEG品質會降低，直到產生符合指定大小的影像，或直到它判斷不符合為止。 在後一種情況下，請求失敗並出現錯誤。

值0表示響應不受大小限制。

不允許負值。

## 屬性 {#section-19e544e77d35478b98fe8666f27d6968}

請求屬性。 不論目前的圖層設定如何，都適用。 如果輸出影像格式不是JPEG，則忽略。

## 預設 {#section-198b798ed187453197e0969c641d6fb5}

0

## 範例 {#section-46bf806fd3ef4875b7726df32b6f834d}

保證大小不會太大，無法傳送至記憶體有限的裝置：

`http://server/myRoodId/myImageId?qlt=60&wid=300&jpegSize=10`

## 另請參閱 {#section-98d472b39d6547969fce6dd86748c153}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) ，屬 [性：:JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
