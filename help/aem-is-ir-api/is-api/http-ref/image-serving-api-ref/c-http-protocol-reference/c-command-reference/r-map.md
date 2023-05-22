---
description: 影像映射資料。 提供此圖層的影像映射資料。 覆蓋此層的目錄映射中的任何資料。
solution: Experience Manager
title: 地圖
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7c1fbb50-98ec-4d9a-b608-93d60d687069
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 2%

---

# 地圖{#map}

影像映射資料。 提供此圖層的影像映射資料。 覆蓋目錄：:Map中此層的所有資料。

`map=[ *`字串`*]mapA=[ *`字串A`*]`

<table id="simpletable_2E32B25D5F6246A18A8AF817903877ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 字串</span></span> </p></td> 
  <td class="stentry"> <p>圖層坐標中此圖層的影像映射資料。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 字串A</span></span> </p></td> 
  <td class="stentry"> <p>源影像坐標中此層的影像映射資料。 </p></td> 
 </tr> 
</table>

空字串表示此圖層不應提供影像映射。 字串必須正確使用HTTP編碼以避免分析問題。

在中出現的所有和符(&amp;)字元 *`string`* 必須是http編碼。

同時 `mapA=` 和 `catalog::Map` 在源影像坐標中指定地圖資料， `map=` 假定圖層坐標相對於圖層矩形的左上角(在 `rotate=` 和 `extend=` 已應用)。

輸出影像映射始終被剪切到圖層矩形。 如果 `shape` 屬性省略或設定為 `default`，整個圖層矩形用作影像映射區。

## 屬性 {#section-a18d9ea95c71414a905a68b8839c0843}

層屬性。 應用到時 `layer=comp`，指定的映射資料分層在所有其他影像映射之後。 忽略，除非 `req=map`。 被效果層忽略。 `mapA=` 如果忽略 `map=` 。

## 預設 {#section-620c19b3f3b84ba49706062de3f12f05}

`catalog::Map` 如果 `map=` 未指定。

## 範例 {#section-cd7691c94f984222845c86dcb0051ce8}

為簡單文本圖層定義矩形影像映射：

`…&layer=1&text=Scene7&map=<area%20alt=Scene7%20href=www.scene7.com>&…`

安 `AREA` 具有（大多）預設屬性的元素用於插入整個圖層矩形的映射區。

## 另請參閱 {#section-bc1d946fdf4b47bf9742a986800aa9b5}

[影像映射](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab)。 [req=map](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
