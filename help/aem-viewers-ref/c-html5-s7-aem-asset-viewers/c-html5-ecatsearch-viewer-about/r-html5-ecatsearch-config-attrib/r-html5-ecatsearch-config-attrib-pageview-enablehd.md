---
description: PageView.enableHD
solution: Experience Manager
title: PageView.enableHD
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 3%

---


# PageView.enableHD{#pageview-enablehd}

[!DNL `[PageView.|<containerId>_pageView.]enableHD=always|never|limit[, *`數字`*]`]

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> 對<span class="codeph"> devicePixelRatio</span>大於<span class="codeph"> 1</span>的裝置啟用、限制或停用最佳化，即具有高密度顯示（如iPhone4）和類似裝置的裝置。 如果處於活動狀態，則元件將限制IS影像請求的大小，好像設備只具有<span class="codeph"> 1</span>的像素比例，並通過這種方式減少頻寬。 </p> <p>請參閱下列範例 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 數字</span></span> </p> </td> 
   <td colname="col2"> <p> 如果使用限制設定，元件僅會啟用高像素密度，而達到指定的限制。 </p> <p>請參閱下列範例。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-38b878e38caa439bb462d4fa637afdaa}

選填。

## 預設 {#section-50b22de303c1432094530e6583132c02}

`limit,1500`

## 範例 {#section-09433488774245d985acef6c0341ece0}

以下是當您搭配檢視器使用此設定屬性時的預期結果，檢視器大小為1000 x 1000:

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
   <td colname="col2"> <p>螢幕／設備的像素密度始終被考慮在內。 </p> <p> 
     <ul id="ul_D8F31FDFCDB74B75A3B1BFBEE33AF2E2"> 
      <li id="li_8A1C6DCCE10545349C73029729211BB2"> <p>如果螢幕像素密度= 1，則要求的影像為1000 x 1000。 </p> </li> 
      <li id="li_884156A34AC64B4E9B3ACC4C25EB710F"> <p>如果螢幕像素密度= 1.5，則要求的影像是1500 x 1500。 </p> </li> 
      <li id="li_7EC699284A7F4E679E512C3DA8B5454F"> <p>如果螢幕像素密度= 2，則要求的影像為2000 x 2000。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 永不</span> </p> </td> 
   <td colname="col2"> <p>它一律使用像素密度1，而忽略裝置的HD功能。 因此，請求的影像一律為1000 x 1000。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 限制&lt;number&gt;</span> </p> </td> 
   <td colname="col2"> <p>請求裝置像素密度，並且僅當產生的影像低於指定的限制時才提供。 </p> <p>限制編號適用於寬度或高度尺寸。 </p> <p> 
     <ul id="ul_CEC06B2280164951BA1A0ADED99E8050"> 
      <li id="li_CA7A0980ACC54690A4F212DF53E2DC8A"> <p>如果限制數為1600，而像素密度為1.5，則會提供1500 x 1500影像。 </p> </li> 
      <li id="li_A4AAD7FBFA0347B082789511CA6768A5"> <p>如果限制數為1600，而像素密度為2，則1000 x 1000影像會因為2000 x 2000影像超過限制而提供。 </p> </li> 
     </ul> </p> <p><b>最佳實務</b>:限制編號必須與公司設定搭配運作，以取得最大尺寸的影像。因此，請將限制數設為等於公司影像大小上限設定。 </p> </td> 
  </tr> 
 </tbody> 
</table>

