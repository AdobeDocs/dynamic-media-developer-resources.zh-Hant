---
title: 地圖
description: 影像地圖資料。 提供此圖層的影像地圖資料。 覆寫來自此圖層之目錄地圖的任何資料。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7c1fbb50-98ec-4d9a-b608-93d60d687069
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 2%

---

# 地圖{#map}

影像地圖資料。 提供此圖層的影像地圖資料。 覆寫此圖層的catalog：：Map中的所有資料。

`map=[ *`字串`*]mapA=[ *`字串A`*]`

<table id="simpletable_2E32B25D5F6246A18A8AF817903877ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">字串</span></span> </p></td> 
  <td class="stentry"> <p>圖層座標中此圖層的影像地圖資料。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">字串A</span></span> </p></td> 
  <td class="stentry"> <p>此圖層的影像地圖資料（以來源影像座標表示）。 </p></td> 
 </tr> 
</table>

空白字串表示此圖層不應提供影像地圖。 字串必須正確以HTTP編碼，以避免剖析問題。

在&#x200B;*`string`*&#x200B;中出現的所有與號(&amp;)字元都必須使用http編碼。

當`mapA=`和`catalog::Map`以來源影像座標指定地圖資料時，`map=`會假設圖層座標是相對於圖層矩形左上角（套用`rotate=`和`extend=`之後）。

輸出影像對應一律會裁剪至圖層矩形。 如果省略`shape`屬性或設為`default`，則會使用整個圖層矩形做為影像地圖區域。

## 屬性 {#section-a18d9ea95c71414a905a68b8839c0843}

圖層屬性。 當套用至`layer=comp`時，指定的地圖資料會分層到所有其他影像地圖之後。 已忽略，除非`req=map`。 被效果圖層忽略。 如果已指定`map=`，則會略過`mapA=`。

## 預設 {#section-620c19b3f3b84ba49706062de3f12f05}

如果未指定`map=`，則使用`catalog::Map`。

## 範例 {#section-cd7691c94f984222845c86dcb0051ce8}

定義簡單文字圖層的矩形影像地圖：

`…&layer=1&text=Scene7&map=<area%20alt=Scene7%20href=www.scene7.com>&…`

具有（大部分）預設屬性的`AREA`元素可用來插入整個圖層矩形的對映區域。

## 另請參閱 {#section-bc1d946fdf4b47bf9742a986800aa9b5}

[影像地圖](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab)，[req=map](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
