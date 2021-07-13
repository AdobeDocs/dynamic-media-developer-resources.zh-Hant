---
description: ZoomView.enableHD
solution: Experience Manager
title: ZoomView.enableHD
feature: Dynamic Media Classic，檢視器，SDK/API，縮放
role: Developer,User
exl-id: 321ca7e2-e3f9-4b0e-8bde-41d8478e1a0b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 2%

---

# ZoomView.enableHD{#zoomview-enablehd}

` [ZoomView.|<containerId>_zoomView.]enableHD=always|never|limit[, *`數字`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 一律|從不|限制</span> </p> </td> 
   <td colname="col2"> <p> 對<span class="codeph"> devicePixelRatio</span>大於<span class="codeph"> 1</span>的設備啟用、限制或禁用優化，即具有高密度顯示的設備，如iPhone4和類似設備。 如果活動，則元件將限制IS影像請求的大小，就像設備只有<span class="codeph"> 1</span>的像素比，這樣可以減少頻寬。 </p> <p>請參閱下列範例。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 數字</span> </span> </p> </td> 
   <td colname="col2"> <p> 如果使用限制設定，元件僅會啟用高像素密度，而最高可達指定的限制。 </p> <p>請參閱下列範例。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-50bcd15223174bb79ce08b31ea03d682}

選填。

## 預設 {#section-7564169749ff4a4996049ea1148cb2a5}

`limit,1500`

## 範例 {#section-96e69b70365f461dae4399e49044ea2f}

將此配置屬性與查看器一起使用時，如果查看器大小為1000 x 1000，則預期結果如下：

<table id="table_F97FEDA0EE1B4EF6AC9FF9060548ACA4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>如果設定變數等於 </p> </th> 
   <th colname="col2" class="entry"> <p>結果 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 始終</span> </p> </td> 
   <td colname="col2"> <p>始終考慮螢幕/設備的像素密度。 </p> <p> 
     <ul id="ul_D8F31FDFCDB74B75A3B1BFBEE33AF2E2"> 
      <li id="li_8A1C6DCCE10545349C73029729211BB2"> <p>如果螢幕像素密度= 1，則請求的影像為1000 x 1000。 </p> </li> 
      <li id="li_884156A34AC64B4E9B3ACC4C25EB710F"> <p>如果螢幕像素密度= 1.5，則請求的影像為1500 x 1500。 </p> </li> 
      <li id="li_7EC699284A7F4E679E512C3DA8B5454F"> <p>如果螢幕像素密度= 2，則請求的影像為2000 x 2000。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 永不</span> </p> </td> 
   <td colname="col2"> <p>它一律會使用1的像素密度，並忽略裝置的硬碟功能。 因此，請求的映像始終為1000 x 1000。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 限制&lt;number&gt;</span> </p> </td> 
   <td colname="col2"> <p>僅當產生的影像低於指定限制時，才請求和提供設備像素密度。 </p> <p>限制編號適用於寬度或高度尺寸。 </p> <p> 
     <ul id="ul_CEC06B2280164951BA1A0ADED99E8050"> 
      <li id="li_CA7A0980ACC54690A4F212DF53E2DC8A"> <p>如果限制數為1600，像素密度為1.5，則提供1500 x 1500影像。 </p> </li> 
      <li id="li_A4AAD7FBFA0347B082789511CA6768A5"> <p>如果限制數為1600，而像素密度為2，則1000 x 1000影像將被提供，因為2000 x 2000影像超過了限制。 </p> </li> 
     </ul> </p> <p> <b>最佳實務</b>:限制編號必須與公司設定搭配使用，以設定最大大小影像。因此，請將限制數量設定為等於公司最大影像大小設定。 </p> </td> 
  </tr> 
 </tbody> 
</table>
