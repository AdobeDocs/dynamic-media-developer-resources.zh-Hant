---
description: 影像地圖資料。 提供此圖層的影像地圖資料。 覆寫此圖層的目錄映射中的任何資料。
solution: Experience Manager
title: 地圖
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 3%

---


# 地圖{#map}

影像地圖資料。 提供此圖層的影像地圖資料。 覆寫目錄：：此圖層的映射中的任何資料。

`map=[ *`字`*]mapA=[ *`串A`*]`

<table id="simpletable_2E32B25D5F6246A18A8AF817903877ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 字串</span></span> </p></td> 
  <td class="stentry"> <p>圖層座標中此圖層的影像地圖資料。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> stringA</span></span> </p></td> 
  <td class="stentry"> <p>在源影像坐標中此圖層的影像映射資料。 </p></td> 
 </tr> 
</table>

空字串表示此圖層不應提供影像地圖。 字串必須正確使用HTTP編碼，以避免剖析問題。

*`string`*&#x200B;中發生的所有&amp;符號字元都必須使用http編碼。

當`mapA=`和`catalog::Map`在來源影像座標中指定地圖資料時，`map=`會假設圖層座標相對於圖層矩形的左上角（在`rotate=`和`extend=`已套用後）。

輸出影像地圖一律會剪裁到圖層矩形。 如果省略`shape`屬性或設為`default`，則整個圖層矩形會用作影像地圖區域。

## 屬性 {#section-a18d9ea95c71414a905a68b8839c0843}

層屬性。 當套用至`layer=comp`時，指定的地圖資料會分層在所有其他影像地圖後面。 忽略，除非`req=map`。 被效果圖層忽略。 `mapA=` 如果也指 `map=` 定，則忽略。

## 預設 {#section-620c19b3f3b84ba49706062de3f12f05}

`catalog::Map` 的值。 `map=` 

## 範例 {#section-cd7691c94f984222845c86dcb0051ce8}

為簡單的文字圖層定義矩形影像地圖：

`…&layer=1&text=Scene7&map=<area%20alt=Scene7%20href=www.scene7.com>&…`

`AREA`元素包含（大部分）預設屬性，用來插入整個圖層矩形的對應區域。

## 另請參閱 {#section-bc1d946fdf4b47bf9742a986800aa9b5}

[影像地圖](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab),  [req=map](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
