---
description: 重新取樣模式。 選擇重新取樣和／或插值算法用於縮放影像資料。 此外，在檢視變形期間，也會套用至文字圖層的旋轉和複合影像的大小調整。
solution: Experience Manager
title: resMode
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 63c1c028-0378-4a38-8018-e358491786d8
translation-type: tm+mt
source-git-commit: b08d1f5b0aa512be4a6e6a4d45d8d4dec15ca1db
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 2%

---

# resMode{#resmode}

重新取樣模式。 選擇重新取樣和／或插值算法用於縮放影像資料。 此外，在檢視變形期間，也會套用至文字圖層的旋轉和複合影像的大小調整。

`resMode=bilin|bicub|sharp2|bisharp`

<table id="table_FD658AC521E24EB9ADBB87F98549BC3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bilin  </span> </p> </td> 
   <td colname="col2"> <p>選擇標準雙線性插值。 最快速的重新取樣方法；有些鋸齒不自然現象很明顯。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bicub  </span> </p> </td> 
   <td colname="col2"> <p>選擇雙三次插值。 比雙線性插值耗用的CPU資源更多，但產生的影像更銳利，而且鋸齒不自然效果也更明顯。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sharp2  </span> </p> </td> 
   <td colname="col2"> <p>選擇修改的Lanczos窗口函式作為插值算法。 在CPU成本較高的情況下，產生比雙立方體更銳利的結果。 <span class="codeph"> sharp已 </span> 由sharp2取代， <span class="codeph"> 其造成鋸齒偽影的可能性 </span>較低(Moiré)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 比沙爾普  </span> </p> </td> 
   <td colname="col2"> <p>選擇Photoshop預設的重採樣器以減小在Adobe Photoshop稱為「雙立方體銳利化」的影像大小。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!IMPORTANT]
>
>若要在您同時使用`resMode=bisharp`和`fit=stretch`時維持影像的高寬比，最好使用width參數或height參數。 如果必須定義兩個參數，則可將它們包在不同的層中，如下例所示：
>
>`/is/image/is/image/companyname?layer=0&src=is(companyname/imagename?wid=30&hei=30&fit=stretch)&resmode=bisharp`

## 屬性 {#section-a171bacf4ddf43c782e46b86a16d443e}

請求屬性。 套用至建立最終回覆影像時涉及的所有縮放操作，包括所有圖層縮放。

## 預設 {#section-d5e1b26f5703461395018a3a627f7283}

`attribute::ResMode`

## 範例 {#section-ee8c3e5a2e3845fe81de5073a8ab7efe}

擷取儲存在影像目錄中之圖層影像的最佳品質轉譯。 影像可包含文字。 該影像將在影像編輯應用中進一步處理，並因此請求具有該影像的Alpha通道。

` http:// *`伺服器`*/myLayeredImage?fmt=tif-alpha,,lzw&resMode=sharp2&wid=1800`

## 另請參閱 {#section-5f7b17f66bc940d197f8e77e6b4f9657}

[屬性：:ResMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
