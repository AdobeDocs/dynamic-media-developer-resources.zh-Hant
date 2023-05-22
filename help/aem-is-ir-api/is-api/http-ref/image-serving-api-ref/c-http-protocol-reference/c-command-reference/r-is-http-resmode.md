---
title: resMode
description: 重新取樣模式。 選擇要用於縮放影像資料的重採樣和/或插值算法。 還適用於視圖轉換期間文本圖層的旋轉和複合影像的大小調整。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 63c1c028-0378-4a38-8018-e358491786d8
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 2%

---

# resMode{#resmode}

重新取樣模式。 選擇要用於縮放影像資料的重採樣和/或插值算法。 還適用於視圖轉換期間文本圖層的旋轉和複合影像的大小調整。

`resMode=bilin|bicub|sharp2|bisharp`

<table id="table_FD658AC521E24EB9ADBB87F98549BC3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 比林 </span> </p> </td> 
   <td colname="col2"> <p>選擇標準雙線性插值。 快速重採樣方法；有些鋸齒偽影是可以察覺的。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 比克 </span> </p> </td> 
   <td colname="col2"> <p>選擇雙三次插值。 與雙線性插值相比，CPU密集程度更高，但生成的影像更清晰，鋸齒偽像更少。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 銳2 </span> </p> </td> 
   <td colname="col2"> <p>選擇修改的Lanczos窗函式作為插值算法。 在CPU成本較高的情況下，結果比雙立方的結果更清晰。 <span class="codeph"> 鋒利 </span> 已替換為 <span class="codeph"> 銳2 </span>)，其導致鋸齒偽影的可能性較小(Moiré)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 比沙爾 </span> </p> </td> 
   <td colname="col2"> <p>選擇Photoshop預設重採樣器以減小在Adobe Photoshop中稱為「雙三次銳化」的影像大小。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!IMPORTANT]
>
>使用兩者時維護影像的長寬比 `resMode=bisharp` 和 `fit=stretch`最好使用寬度參數或高度參數。 如果必須定義兩個參數，則可以將它們換到不同的層，如下例所示：
>
>`/is/image/is/image/companyname?layer=0&src=is(companyname/imagename?wid=30&hei=30&fit=stretch)&resmode=bisharp`

## 屬性 {#section-a171bacf4ddf43c782e46b86a16d443e}

請求屬性。 適用於建立最終回復影像時涉及的所有縮放操作，包括所有圖層縮放。

## 預設 {#section-d5e1b26f5703461395018a3a627f7283}

`attribute::ResMode`

## 範例 {#section-ee8c3e5a2e3845fe81de5073a8ab7efe}

檢索儲存在影像目錄中的分層影像的最佳質量再現。 影像可以包含文本。 在影像編輯應用中進一步處理該影像，並因此請求具有該影像的α通道。

` http:// *`伺服器`*/myLayeredImage?fmt=tif-alpha,,lzw&resMode=sharp2&wid=1800`

## 另請參閱 {#section-5f7b17f66bc940d197f8e77e6b4f9657}

[屬性：:ResMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
