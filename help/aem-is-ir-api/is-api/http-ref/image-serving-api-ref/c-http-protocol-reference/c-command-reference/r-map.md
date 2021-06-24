---
description: 影像地圖資料。 提供此層的影像映射資料。 覆寫此層的目錄映射中的任何資料。
solution: Experience Manager
title: 地圖
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 7c1fbb50-98ec-4d9a-b608-93d60d687069
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 3%

---

# 地圖{#map}

影像地圖資料。 提供此層的影像映射資料。 覆寫此層的目錄：:Map中的任何資料。

`map=[ *``*]mapA=[ *`stringstringA`*]`

<table id="simpletable_2E32B25D5F6246A18A8AF817903877ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 字串</span></span> </p></td> 
  <td class="stentry"> <p>在圖層坐標中為此圖層映射資料。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> stringA</span></span> </p></td> 
  <td class="stentry"> <p>在源影像坐標中為此層映像資料。 </p></td> 
 </tr> 
</table>

空字串表示此層不應提供影像映射。 字串必須正確以HTTP編碼，以避免剖析問題。

*`string`*&#x200B;中出現的所有&amp;字元都必須進行http編碼。

當`mapA=`和`catalog::Map`在源影像坐標中指定映射資料時，`map=`假定層坐標相對於層矩形的左上角（在`rotate=`和`extend=`已應用後）。

輸出影像映射始終被剪切到圖層矩形。 如果省略`shape`屬性或將其設定為`default`，則整個圖層矩形將用作影像映射區。

## 屬性 {#section-a18d9ea95c71414a905a68b8839c0843}

層屬性。 當應用到`layer=comp`時，指定的映射資料將分層到所有其他影像映射後面。 忽略，除非`req=map`。 被效果層忽略。 `mapA=` 也會 `map=` 忽略。

## 預設 {#section-620c19b3f3b84ba49706062de3f12f05}

`catalog::Map` 若未指定， `map=` 則會使用。

## 範例 {#section-cd7691c94f984222845c86dcb0051ce8}

為簡單文本層定義矩形影像映射：

`…&layer=1&text=Scene7&map=<area%20alt=Scene7%20href=www.scene7.com>&…`

`AREA`元素（大多）具有預設屬性，用於插入整個圖層矩形的映射區域。

## 另請參閱 {#section-bc1d946fdf4b47bf9742a986800aa9b5}

[影像地圖](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab),  [req=map](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
