---
title: ZoomView.enableHD
description: ZoomView.enableHD
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 321ca7e2-e3f9-4b0e-8bde-41d8478e1a0b
source-git-commit: 61e3a1fd0e21d336eaf5232096f5b1b54f2a6353
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 2%

---

# ZoomView.enableHD{#zoomview-enablehd}

` [ZoomView.|<containerId>_zoomView.]enableHD=always|never|limit[, *`數字`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 始終|never|limit</span> </p> </td> 
   <td colname="col2"> <p> 對以下設備啟用、限制或禁用優化 <span class="codeph"> 設備PixelRatio</span> 大於 <span class="codeph"> 1</span>這就是像iPhone4和類似的器件一樣，具有高密度顯示的器件。 如果處於活動狀態，則元件將限制IS影像請求的大小，就好像設備僅具有像素比 <span class="codeph"> 1</span> 減少頻寬。 </p> <p>請參見下例。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 數</span> </span> </p> </td> 
   <td colname="col2"> <p> 如果使用限制設定，則元件僅允許高像素密度達到指定的限制。 </p> <p>請參見下例。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-50bcd15223174bb79ce08b31ea03d682}

選擇性.

## 預設 {#section-7564169749ff4a4996049ea1148cb2a5}

`limit,1500`

## 範例 {#section-96e69b70365f461dae4399e49044ea2f}

以下是將此配置屬性與查看器一起使用時的預期結果，查看器大小為1000 x 1000:

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
   <td colname="col2"> <p>螢幕/設備的像素密度始終被計算。</p> <p> 
     <ul id="ul_D8F31FDFCDB74B75A3B1BFBEE33AF2E2"> 
      <li id="li_8A1C6DCCE10545349C73029729211BB2"> <p>如果螢幕像素密度= 1，則請求的影像為1000 x 1000。 </p> </li> 
      <li id="li_884156A34AC64B4E9B3ACC4C25EB710F"> <p>如果螢幕像素密度= 1.5，則請求的影像為1500 x 1500。 </p> </li> 
      <li id="li_7EC699284A7F4E679E512C3DA8B5454F"> <p>如果螢幕像素密度= 2，則請求的影像為2000 x 2000。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 永不</span> </p> </td> 
   <td colname="col2"> <p>它始終使用1的像素密度，而忽略設備的高清功能。 因此，請求的映像總是1000 x 1000。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 限&lt;number&gt;</span> </p> </td> 
   <td colname="col2"> <p>僅當得到的影像低於指定限制時才請求和提供設備像素密度。 </p> <p>限制編號適用於寬度或高度尺寸。 </p> <p> 
     <ul id="ul_CEC06B2280164951BA1A0ADED99E8050"> 
      <li id="li_CA7A0980ACC54690A4F212DF53E2DC8A"> <p>若限制數為1600，像素密度為1.5，則提供1500×1500的影像。 </p> </li> 
      <li id="li_A4AAD7FBFA0347B082789511CA6768A5"> <p>如果限制數為1600，像素密度為2，則1000 x 1000影像由於2000 x 2000影像超過限制而被提供。 </p> </li> 
     </ul> </p> <p> <b>最佳實踐</b>:限制編號必須與最大大小映像的公司設定一起使用。 因此，將限制編號設定為等於公司最大影像大小設定。 </p> </td> 
  </tr> 
 </tbody> 
</table>
