---
description: 透視變形。 對圖層來源影像套用透視變形，以填滿以四邊形指定的區域。 圖層的其他區域保持透明。
solution: Experience Manager
title: 透視
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 2%

---


# perspective&lt;a0/{#perspective}

透視變形。 對圖層來源影像套用透視變形，以填滿以四邊形指定的區域。 圖層的其他區域保持透明。

`perspective= *`perspQuadres`*[, *`選項`*]`

`perspectiveN= *`perspQuadNresOptions`*[, *``*]`

<table id="simpletable_4BD38BBF53964F7D97B9E58914C97B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuad</span> </p></td> 
  <td class="stentry"> <p>透視四邊形像素座標（8個以逗號分隔）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuadN</span> </p></td> 
  <td class="stentry"> <p>透視四邊形標準化座標（8以逗號分隔）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> resOptions</span> </p></td> 
  <td class="stentry"> <p>重新取樣選項（請參閱下面）。 </p></td> 
 </tr> 
</table>

*`perspQuad`* 由複合（或圖層0）坐標空間中的四個像素坐標值組成，這些值起源於複合影像的左上角。

`perspQuadN` 由四個標準化的坐標值組成， `0.0,0.0` 其中對應於複合／圖層0影像的左上 `1.0,1.0` 角和右下角。

轉換輸入影像，使輸入影像的左上角映射到`perspQuad[N]`的第一坐標值，右上角到第二坐標，右下角到第三坐標，左下角到第四坐標。

>[!NOTE]
>
>`pos=` 可用於進一步定位複合影像中的變換層。

透視四邊形座標可位於複合影像外部。

如果四邊形不適合透視變換（例如，如果兩個或多個頂點重合，如果三個或所有頂點位於同一行上，或者四邊形是自相交或凹），則行為未定義。

## 質量注意事項{#section-7cc9056afa614300a9b8844d39739fc3}

雖然預設實作會在品質與效能之間產生合理的折中，但有時可能需要增加來源影像的解析度，以改善清晰度或減少鋸齒不自然現象。

如果源是影像，請使用`scale=`選擇不同的解析度（相對於影像的完整解析度）。 指定的`scale=`值會四捨五入到下一個較高的PTIF解析度級別。 在巢狀請求源的情況下，可調整由巢狀請求產生的影像的大小以獲得所需的清晰度。 對於文本層，通過選擇較大的大小=值並同時增加以`textAttr=`指定的解析度來調整輸入影像（渲染文本）的解析度。

*`resOptions`* 允許選取替代的重新取樣演算法。支援下列值（區分大小寫）:

<table id="table_0F20007986324E228096888ED37219C0"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 值</b> </th> 
   <th class="entry"> <b> 說明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> R1</span> </p> </td> 
   <td> <p> 最近的鄰居。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R2</span> </p> </td> 
   <td> <p> 雙線性式. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R3</span> </p> </td> 
   <td> <p> 標準超級取樣（預設）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">R3<span class="varname"> Tn</span></span> </p> </td> 
   <td> <p> 具有可調抖動的超採樣（<span class="varname"> n</span>必須是0到200之間的整數值）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-818e57df0a1b4449888543bc6af77751}

圖層命令。 應用於當前層，如果`layer=comp`則應用於層0。 被效果圖層忽略。

`res=` 在相同圖層中顯示透視時，一律忽略。`size=` 在為影像圖層指定時會忽略。`size=` 和 `res=` 含有的圖層 `perspective=` 保留供日後使用。

## 預設 {#section-e35683395d514d4eb6b32924e1bf8f2f}

`None`，以取消透視變形。

## 另請參閱 {#section-e5b71ac4a0724df6bf678dd354cfa51a}

[size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b) ,  [scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065),  [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143),  [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)
