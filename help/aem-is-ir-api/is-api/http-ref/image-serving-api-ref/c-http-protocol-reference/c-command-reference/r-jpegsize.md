---
description: JPEG大小（以千位元組為單位）。 指定JPEG響應的最大大小(KB)。
solution: Experience Manager
title: jpeg大小
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08cecb09-100f-4671-b335-d59c88b0e1ef
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 3%

---

# jpeg大小{#jpegsize}

JPEG大小（以千位元組為單位）。 指定JPEG響應的最大大小(KB)。

`jpegSize= *`大小`*`

<table id="simpletable_EC2A8D8B65854B45B9CB184DA1069355"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 大小</span></span> </p> </td> 
  <td class="stentry"> <p>大小(KB)。 </p></td> 
 </tr> 
</table>

如果此值設定為正值，並且具有指定JPEG質量的JPEG響應未超過此值，則該影像作為響應返回。 否則，JPEG質量會降低，直到它生成適合指定大小的影像或確定它不能適合。 在後一種情況下，請求失敗並出現錯誤。

值0表示響應不受大小限制。

不允許使用負值。

## 屬性 {#section-19e544e77d35478b98fe8666f27d6968}

請求屬性。 應用，與當前圖層設定無關。 如果輸出影像格式不是JPEG，則忽略。

## 預設 {#section-198b798ed187453197e0969c641d6fb5}

0

## 範例 {#section-46bf806fd3ef4875b7726df32b6f834d}

確保大小不會太大，無法傳送到記憶體有限的設備：

`http://server/myRoodId/myImageId?qlt=60&wid=300&jpegSize=10`

## 另請參閱 {#section-98d472b39d6547969fce6dd86748c153}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) 。 [屬性：:JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
