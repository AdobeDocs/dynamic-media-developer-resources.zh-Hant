---
title: 解析模式
description: 重新取樣模式。 選擇要用於縮放影像資料的重新取樣和/或內插演演算法。 也適用於在檢視轉換期間文字圖層的旋轉和複合影像大小調整。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 63c1c028-0378-4a38-8018-e358491786d8
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 1%

---

# 解析模式{#resmode}

重新取樣模式。 選擇要用於縮放影像資料的重新取樣和/或內插演演算法。 也適用於在檢視轉換期間文字圖層的旋轉和複合影像大小調整。

`resMode=bilin|bicub|sharp2|bisharp`

<table id="table_FD658AC521E24EB9ADBB87F98549BC3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bilin </span> </p> </td> 
   <td colname="col2"> <p>選取標準的雙線性內插。 最快速的重新取樣方法；會產生某些明顯的鋸齒狀不自然感。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bicub </span> </p> </td> 
   <td colname="col2"> <p>選取雙三次插值法。 CPU比雙線性內插運算密集得多，但會產生較清晰的影像，且鋸齒狀不自然感較不明顯。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sharp2 </span> </p> </td> 
   <td colname="col2"> <p>選取修改過的Lanczos視窗函式作為內插演演算法。 可以產生比雙立方體稍微銳利的結果，但成本較高CPU。 <span class="codeph"> sharp </span>已由<span class="codeph"> sharp2 </span>取代，這造成鋸齒狀成品(Moiré)的可能性較小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">個兩次銳利化</span> </p> </td> 
   <td colname="col2"> <p>選取Photoshop預設的重新取樣器，以縮減影像大小(在Adobe Photoshop中稱為「雙立方銳利化」)。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!IMPORTANT]
>
>當您同時使用`resMode=bisharp`和`fit=stretch`時，若要維持影像的外觀比例，最好使用width引數或height引數。 如果必須定義這兩個引數，您可以將其換成不同的圖層，如下列範例所示：
>
>`/is/image/is/image/companyname?layer=0&src=is(companyname/imagename?wid=30&hei=30&fit=stretch)&resmode=bisharp`

## 屬性 {#section-a171bacf4ddf43c782e46b86a16d443e}

要求屬性。 適用於建立最終回覆影像時涉及的所有縮放操作，包括所有圖層縮放。

## 預設 {#section-d5e1b26f5703461395018a3a627f7283}

`attribute::ResMode`

## 範例 {#section-ee8c3e5a2e3845fe81de5073a8ab7efe}

擷取影像目錄中儲存之圖層影像的最佳品質轉譯。 影像可以包含文字。 影像會在影像編輯應用程式中進一步處理，因此要求影像有Alpha色版。

` http:// *`伺服器`*/myLayeredImage?fmt=tif-alpha,,lzw&resMode=sharp2&wid=1800`

## 另請參閱 {#section-5f7b17f66bc940d197f8e77e6b4f9657}

[attribute：：ResMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
