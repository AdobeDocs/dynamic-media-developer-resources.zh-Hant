---
description: PageView.enableHD
solution: Experience Manager
title: PageView.enableHD
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 394b79cd-0611-4496-86e3-366a2ffc6ca7
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 2%

---

# PageView.enableHD{#pageview-enablehd}

[!DNL `[PageView.|<containerId>_pageView.]enableHD=always|never|limit[, *`數字`*]`]

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 始終|never|limit</span> </p> </td> 
   <td colname="col2"> <p> 對以下設備啟用、限制或禁用優化 <span class="codeph"> 設備PixelRatio</span> 大於 <span class="codeph"> 1</span>這就是像iPhone4和類似的器件一樣，具有高密度顯示的器件。 如果處於活動狀態，則元件將限制IS影像請求的大小，就好像設備僅具有像素比 <span class="codeph"> 1</span> 減少頻寬。 </p> <p>請參閱下面的示例 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 數字</span></span> </p> </td> 
   <td colname="col2"> <p> 如果使用限制設定，則元件僅允許高像素密度達到指定的限制。 </p> <p>請參見下例。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-38b878e38caa439bb462d4fa637afdaa}

選擇性.

## 預設 {#section-50b22de303c1432094530e6583132c02}

`limit,1500`

## 範例 {#section-09433488774245d985acef6c0341ece0}

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
   <td colname="col1"> <p><span class="codeph"> 始終</span> </p> </td> 
   <td colname="col2"> <p>螢幕/設備的像素密度總是被考慮。 </p> <p> 
     <ul id="ul_D8F31FDFCDB74B75A3B1BFBEE33AF2E2"> 
      <li id="li_8A1C6DCCE10545349C73029729211BB2"> <p>如果螢幕像素密度= 1，則請求的影像為1000 x 1000。 </p> </li> 
      <li id="li_884156A34AC64B4E9B3ACC4C25EB710F"> <p>如果螢幕像素密度= 1.5，則請求的影像為1500 x 1500。 </p> </li> 
      <li id="li_7EC699284A7F4E679E512C3DA8B5454F"> <p>如果螢幕像素密度= 2，則請求的影像為2000 x 2000。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 永不</span> </p> </td> 
   <td colname="col2"> <p>它始終使用1的像素密度，而忽略設備的高清功能。 因此，請求的映像總是1000 x 1000。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 限&lt;number&gt;</span> </p> </td> 
   <td colname="col2"> <p>僅當得到的影像低於指定限制時才請求和提供設備像素密度。 </p> <p>限制編號適用於寬度或高度尺寸。 </p> <p> 
     <ul id="ul_CEC06B2280164951BA1A0ADED99E8050"> 
      <li id="li_CA7A0980ACC54690A4F212DF53E2DC8A"> <p>若限制數為1600，像素密度為1.5，則提供1500×1500的影像。 </p> </li> 
      <li id="li_A4AAD7FBFA0347B082789511CA6768A5"> <p>如果限制數為1600，像素密度為2，則1000 x 1000影像由於2000 x 2000影像超過限制而被提供。 </p> </li> 
     </ul> </p> <p><b>最佳實踐</b>:限制編號需要與最大大小映像的公司設定配合使用。 因此，將限制編號設定為等於公司最大影像大小設定。 </p> </td> 
  </tr> 
 </tbody> 
</table>
