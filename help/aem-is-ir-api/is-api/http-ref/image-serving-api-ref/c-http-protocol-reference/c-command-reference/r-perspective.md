---
description: 透視變換。 將透視變換應用於層源影像，以填充用四邊形指定的區域。 層的其他區域保持透明。
solution: Experience Manager
title: 透視
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2e0297b0-c9a4-4bbd-9f06-368f722288d4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 2%

---

# 透視{#perspective}

透視變換。 將透視變換應用於層源影像，以填充用四邊形指定的區域。 層的其他區域保持透明。

`perspective= *``*[, *`perspQuadresOptions`*]`

`perspectiveN= *``*[, *`perspQuadNresOptions`*]`

<table id="simpletable_4BD38BBF53964F7D97B9E58914C97B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuad</span> </p></td> 
  <td class="stentry"> <p>透視四邊形像素座標（8個real，以逗號分隔）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuadN</span> </p></td> 
  <td class="stentry"> <p>透視四邊形標準化座標（8個標準，以逗號分隔）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> resOptions</span> </p></td> 
  <td class="stentry"> <p>重新取樣選項（請參閱下方）。 </p></td> 
 </tr> 
</table>

*`perspQuad`* 由複合（或層0）坐標空間中的四個像素坐標值組成，這些值源於複合影像的左上角。

`perspQuadN` 由四個標準化坐標值組 `0.0,0.0` 成，其中與複合/層0影像的左上角和右 `1.0,1.0` 下角相對應。

對輸入影像進行變換，使輸入影像的左上角映射到第一坐標值`perspQuad[N]`、右上角到第二坐標、右下角到第三坐標、左下角到第四坐標。

>[!NOTE]
>
>`pos=` 可用於進一步將變換層定位在複合影像中。

透視四邊形坐標可位於複合影像之外。

如果四邊形不適合透視變換（例如，如果兩個或多個頂點重合，如果三個或所有頂點位於同一條線上，或者如果四邊形是自相交或凹面），則行為未定義。

## 品質考量 {#section-7cc9056afa614300a9b8844d39739fc3}

儘管預設實現在質量和效能之間產生合理的折中，但有時可能需要增加源影像的解析度以改進清晰度或減小其以減少混疊偽影。

如果源是影像，請使用`scale=`選擇不同的解析度（相對於影像的完全解析度）。 指定的`scale=`值會四捨五入到下一個較高的PTIF解析度級別。 在巢狀請求源的情況下，可以調整由巢狀請求產生的影像的大小，以達到所需的銳度。 對於文本層，通過選擇較大大小=值並同時增加用`textAttr=`指定的解析度來調整輸入影像（呈現的文本）的解析度。

*`resOptions`* 允許選擇替代的重採樣算法。支援下列值（區分大小寫）:

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
   <td> <p> 標準超級採樣（預設）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">R3<span class="varname"> Tn</span></span> </p> </td> 
   <td> <p> 抖動可調的超採樣（<span class="varname"> n</span>必須是介於0和200之間的整數值）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-818e57df0a1b4449888543bc6af77751}

圖層命令。 應用於當前層，如果`layer=comp`則應用於層0。 被效果層忽略。

`res=` 透視出現在相同層時，一律會忽略。`size=` 為影像層指定時會忽略。`size=` 和 `res=` 在具有的層 `perspective=` 中保留供將來使用。

## 預設 {#section-e35683395d514d4eb6b32924e1bf8f2f}

`None`，而無透視轉換。

## 另請參閱 {#section-e5b71ac4a0724df6bf678dd354cfa51a}

[size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b) ,  [scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065),  [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143),  [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)
