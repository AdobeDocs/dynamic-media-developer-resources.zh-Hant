---
description: 透視轉換。 將透視變換應用於圖層源影像以填充用四邊形指定的區域。 層的其它區域保持透明。
solution: Experience Manager
title: 透視
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2e0297b0-c9a4-4bbd-9f06-368f722288d4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 1%

---

# 透視{#perspective}

透視轉換。 將透視變換應用於圖層源影像以填充用四邊形指定的區域。 層的其它區域保持透明。

`perspective= *`perspQuad`*[, *`res選項`*]`

`perspectiveN= *`perspQuadN`*[, *`res選項`*]`

<table id="simpletable_4BD38BBF53964F7D97B9E58914C97B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuad</span> </p></td> 
  <td class="stentry"> <p>透視四邊形像素坐標（8個標線，用逗號分隔）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuadN</span> </p></td> 
  <td class="stentry"> <p>透視四邊形歸一化坐標（8個標線，用逗號分隔）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> res選項</span> </p></td> 
  <td class="stentry"> <p>重新取樣選項（請參閱下面）。 </p></td> 
 </tr> 
</table>

*`perspQuad`* 由複合（或層0）坐標空間中的四個像素坐標值組成，這些值源於複合影像的左上角。

`perspQuadN` 由四個歸一化坐標值組成，其中 `0.0,0.0` 對應於複合/圖層0影像的左上角， `1.0,1.0` 右下角。

對輸入影像進行變換，使輸入影像的左上角映射到輸入影像的第一坐標值 `perspQuad[N]`，右上角到第二坐標，右下角到第三坐標，左下角到第四坐標。

>[!NOTE]
>
>`pos=` 可用於進一步定位複合影像中的變換層。

透視四邊形坐標可位於複合影像之外。

如果四邊形不適合透視變換（例如，如果兩個或多個頂點重合，如果三個或所有頂點位於同一條線上，或者四邊形是自相交或凹入的），則未定義行為。

## 質量注意事項 {#section-7cc9056afa614300a9b8844d39739fc3}

儘管預設實現在質量和效能之間產生合理的折衷，但有時可能需要提高源影像的解析度以改善清晰度或減小其以減少混疊偽像。

如果源是影像，請使用 `scale=` 選擇其他解析度（相對於影像的全解析度）。 指定的 `scale=` 值四捨五入到下一個較高的PTIF解析度級別。 在嵌套請求源的情況下，可以調整由嵌套請求產生的影像的大小以達到期望的清晰度。 對於文本層，通過選擇較大的大小=值並同時增加指定的解析度來調整輸入影像（渲染文本）的解析度 `textAttr=`。

*`resOptions`* 允許選擇替代重採樣算法。 支援以下值（區分大小寫）:

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
   <td> <p> 雙線性。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R3</span> </p> </td> 
   <td> <p> 標準超採樣（預設）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">R3T<span class="varname"> n</span></span> </p> </td> 
   <td> <p> 具有可調抖動的超採樣(<span class="varname"> n</span> 必須是介於0和200之間的整數值)。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-818e57df0a1b4449888543bc6af77751}

層命令。 應用於當前圖層，如果 `layer=comp`。 被效果層忽略。

`res=` 當透視出現在同一層中時，始終忽略。 `size=` 為影像圖層指定時將忽略。 `size=` 和 `res=` 在層中 `perspective=` 為以後使用而保留。

## 預設 {#section-e35683395d514d4eb6b32924e1bf8f2f}

`None`，以便無透視轉換。

## 另請參閱 {#section-e5b71ac4a0724df6bf678dd354cfa51a}

[大小=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b) 。 [比例=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065)。 [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143)。 [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)
