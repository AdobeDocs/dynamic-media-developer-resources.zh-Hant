---
description: 重新取樣模式。 選擇重新取樣和／或插值算法用於縮放影像資料。 此外，在檢視變形期間，也會套用至文字圖層的旋轉和複合影像的大小調整。
seo-description: 重新取樣模式。 選擇重新取樣和／或插值算法用於縮放影像資料。 此外，在檢視變形期間，也會套用至文字圖層的旋轉和複合影像的大小調整。
seo-title: resMode
solution: Experience Manager
title: resMode
topic: Scene7 Image Serving - Image Rendering API
uuid: 8e12aa06-072c-4e7a-84e6-01437c43c57b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# resMode{#resmode}

重新取樣模式。 選擇重新取樣和／或插值算法用於縮放影像資料。 此外，在檢視變形期間，也會套用至文字圖層的旋轉和複合影像的大小調整。

`resMode=bilin|bicub|sharp2|bisharp`

<table id="table_FD658AC521E24EB9ADBB87F98549BC3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bilin  </span> </p> </td> 
   <td colname="col2"> <p>選擇標準雙線性插值。 最快速的重新取樣方法；可能會有某些明顯的鋸齒狀不自然感。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bicub  </span> </p> </td> 
   <td colname="col2"> <p>選擇雙三次插值。 比雙線性插值耗用的CPU資源更多，但會產生更銳利的影像，而且鋸齒不自然現象也更少。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sharp2  </span> </p> </td> 
   <td colname="col2"> <p>選擇修改的Lanczos窗口函式作為插值算法。 產生的結果可能會比雙立方式稍微銳利一些，但是會耗用較高的 CPU 成本。<span class="codeph"> sharp已 </span> 由sharp2取代， <span class="codeph"> 其造成鋸齒偽影的可能性 </span>較低(Moiré)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 比沙爾普  </span> </p> </td> 
   <td colname="col2"> <p>選擇Photoshop預設重新取樣器，以減少Adobe Photoshop中稱為「雙立方體銳利化」的影像大小。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-a171bacf4ddf43c782e46b86a16d443e}

請求屬性。 套用至建立最終回覆影像時涉及的所有縮放操作，包括所有圖層縮放。

## 預設 {#section-d5e1b26f5703461395018a3a627f7283}

`attribute::ResMode`

## 範例 {#section-ee8c3e5a2e3845fe81de5073a8ab7efe}

擷取儲存在影像目錄中之圖層影像的最佳品質轉譯。 影像可能包含文字。 我們期望在影像編輯應用程式中進一步處理，並因此要求具有影像的alpha色版。

` http:// *`伺服器`*/myLayeredImage?fmt=tif-alpha,,lzw&resMode=sharp2&wid=1800`

## 另請參閱 {#section-5f7b17f66bc940d197f8e77e6b4f9657}

[屬性：:ResMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
