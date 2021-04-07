---
description: 所有檢視器通用的參數。
solution: Experience Manager
title: asset
feature: Dynamic Media經典，檢視器，SDK/API
role: 開發人員，商業從業人員
exl-id: edcd18b6-5292-44da-80be-b7f75ee4c48e
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '585'
ht-degree: 2%

---

# asset{#asset}

所有檢視器通用的參數。

` asset= *`assetId`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> assetId  </span> </span> </p> </td> 
   <td colname="col2"> <p> 單一視訊或最適化視訊集的資產ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>

除非使用`video`參數，否則此屬性為必需屬性。 請參閱「視訊」下方的「外部視訊支援」或「視訊360」下方的「外部視訊支援」。[](../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3)[](../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760)

或

` asset= *`影像`*`

<table id="table_67E18F42E97C4AAAB0A2F67B7924765D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 影像  </span> </span> </p> </td> 
   <td colname="col2"> <p> 指定單一影像或轉盤集。 將雙HTTP編碼套用至影像名稱或轉盤集名稱中任何不安全的字元。 </p> </td> 
  </tr> 
 </tbody> 
</table>

或

` asset= *``* | *``* | *``* | *``* [%3F *`imageimageListimageListListWithModifiersmultiDimensionalSpinSetmodifiers`*]`

<table id="table_A2A0ACD942E942BC99AF0DC80FB1C670"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 影像  </span> </span> </p> </td> 
   <td colname="col2"> <p> 指定單一影像。 將雙HTTP編碼套用至影像名稱中任何不安全的字元。 </p> <p>或者，指定對影像集的引用。 檢視器使用<span class="codeph"> req=set IS </span>請求從伺服器擷取影像集。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> imageList  </span> </span> </p> </td> 
   <td colname="col2"> <p> 指定顯式影像集，由以逗號分隔的排序項或框架序列組成。 </p> <p> <p>注意： 這項功能在AdobeDynamic Media經典中受到支援；Adobe Experience Manager資產不支援。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> imageListWithModifiers  </span> </span> </p> </td> 
   <td colname="col2"> <p> 指定每個影格都有其專屬的「影像伺服」修飾元的明確影像集。 在這種情況下，框架清單會用括弧括住。 請確定您已將雙重HTTP編碼套用至影格特定「影像伺服」修飾元中的任何逗號。 </p> <p> <p>注意： 這項功能在AdobeDynamic Media經典中受到支援；Adobe Experience Manager資產不支援。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> multiDimensionalSpinSet  </span> </span> </p> </td> 
   <td colname="col2"> <p>使用以下語法指定顯式多維回轉集： </p> <p> <span class="codeph"> (( <span class="varname"> horizontalSpinSet </span>)[,(horizontalSpinSet <span class="varname">  </span>)])  </span> </p> <p> 其中<span class="codeph"> <span class="varname"> horizontalSpinSet </span> </span>是指定水準軸以逗號分隔的影格清單。 所有<span class="codeph"> <span class="varname"> horizontalSpinSet </span> </span>應具有相同的幀數。 </p> <p> <p>注意： 這項功能在AdobeDynamic Media經典中受到支援；Adobe Experience Manager資產不支援。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 修飾語  </span> </span> </p> </td> 
   <td colname="col2"> <p> 影像伺服命令；<span class="codeph"> &amp; </span>和<span class="codeph"> = </span>分隔符必須分別以<span class="codeph"> %26 </span>和<span class="codeph"> %3D </span>的HTTP編碼。 </p> </td> 
  </tr> 
 </tbody> 
</table>

或

` asset=( *``* | ( *``*; *``* | *``*; *``* | *``*; *``*); *``*;( *``*; *``* | *``*; *``* | *``*; *``*); *``*;] [%3F *`mediaSetvideoswatchIdmageswatchIdsetIdswatchIdswatchIdIDvideoswatchIdmageswatchIdsetIdswatchIdswatchIdIDmodifiers`*]`

<table id="table_D31C8507C02A4452A79DEDDEC62EF2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> mediaSet  </span> </span> </p> </td> 
   <td colname="col2"> <p> 指定對介質集的引用。 檢視器使用req=set IS請求，從伺服器擷取媒體集。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 視訊  </span> </span> </p> </td> 
   <td colname="col2"> <p> 單一視訊或最適化視訊集。 </p> <p> <p>注意： 這項功能在AdobeDynamic Media經典中受到支援；Adobe Experience Manager資產不支援。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 影像  </span> </span> </p> </td> 
   <td colname="col2"> <p> 單一影像。 </p> <p> <p>注意： 這項功能在AdobeDynamic Media經典中受到支援；Adobe Experience Manager資產不支援。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> setId  </span> </span> </p> </td> 
   <td colname="col2"> <p> 色票集。 </p> <p> <p>注意： 這項功能在AdobeDynamic Media經典中受到支援；Adobe Experience Manager資產不支援。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> swatchId  </span> </span> </p> </td> 
   <td colname="col2"> <p>色票影像。 </p> <p> <p>注意： 這項功能在AdobeDynamic Media經典中受到支援；Adobe Experience Manager資產不支援。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ID  </span> </span> </p> </td> 
   <td colname="col2"> <p> 「媒體集」項目類型標識符可以是以下其中一種： </p> <p> 
     <ul id="ul_3100F9356628498DA820C07F6F69CC9B"> 
      <li id="li_51B649A539F14510873CFDA85A6AA714"> <p> <span class="codeph"> advanced_image  </span> </p> <p>適用於單一影像。 </p> </li> 
      <li id="li_7E764D67294647C1A828F949E5ED1908"> <p> <span class="codeph"> advanced_swatchset  </span> </p> <p>用於嵌套色票集。 </p> </li> 
      <li id="li_C942CED779B54110BCDC74188995FD5B"> <p> <span class="codeph"> 自旋  </span> </p> <p>用於回轉集。 </p> </li> 
      <li id="li_6EA5C54F078D4B24B44F1588BF083842"> <p> <span class="codeph"> 視訊  </span> </p> <p>適用於單一視訊。 </p> </li> 
      <li id="li_8110FA7E0CAB4681A2D8C15F2A656E69"> <p> <span class="codeph"> video_set  </span> </p> <p>適用於最適化視訊集。 </p> </li> 
     </ul> </p> <p> <p>注意： 這項功能在AdobeDynamic Media經典中受到支援；Adobe Experience Manager資產不支援。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 修飾語  </span> </span> </p> </td> 
   <td colname="col2"> <p> 影像伺服命令；<span class="codeph"> &amp; </span>和<span class="codeph"> = </span>分隔符必須分別以<span class="codeph"> %26 </span>和<span class="codeph"> %3D </span>的HTTP編碼。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此檢視器不支援使用IR（影像演算）或UGC（使用者產生的內容）的影像。

## 屬性 {#section-10ee45d637134e0fbcd943c62578cb78}

必要.

## 預設 {#section-d411e450028c460392cb8508f8ccc5d9}

無。

## 範例 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

單一資產參考：

```
asset=Scene7SharedAssets/Backpack_B
```

或

```
asset=/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg
```

或

```
asset=/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4
```

或

```
asset=/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner
```

或

```
asset=Viewers/space_station_360-AVS
```

對目錄中定義的影像集的單一參考：

```
asset=Viewers/Pluralist
```

顯式影像集：

```
asset=Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C
```

使用影格特定影像伺服修飾元的顯式影像集：

```
asset=(Scene7SharedAssets/Backpack_B%3Fop_colorize%3D255%252C0%252C0,Scene7SharedAssets/Backpack_B%3Fop_colorize%3D0x00ff00)
```

對目錄中定義的回轉集的單一參考：

```
asset=Scene7SharedAssets/SpinSet-Sample
```

明確回轉集：

```
asset=Scene7SharedAssets/Frame-1,Scene7SharedAssets/Frame-2,Scene7SharedAssets/Frame-3,Scene7SharedAssets/Frame-4,Scene7SharedAssets/Frame-5,Scene7SharedAssets/Frame-6,Scene7SharedAssets/Frame-7,Scene7SharedAssets/Frame-8
```

顯式多維自旋集：

```
asset=((Scene7SharedAssets/ring1-25,Scene7SharedAssets/ring1-26,Scene7SharedAssets/ring1-27,Scene7SharedAssets/ring1-28,Scene7SharedAssets/ring1-29,Scene7SharedAssets/ring1-30,Scene7SharedAssets/ring1-31,Scene7SharedAssets/ring1-32,Scene7SharedAssets/ring1-33,Scene7SharedAssets/ring1-34,Scene7SharedAssets/ring1-35,Scene7SharedAssets/ring1-36),(Scene7SharedAssets/ring1-13,Scene7SharedAssets/ring1-14,Scene7SharedAssets/ring1-15,Scene7SharedAssets/ring1-16,Scene7SharedAssets/ring1-17,Scene7SharedAssets/ring1-18,Scene7SharedAssets/ring1-19,Scene7SharedAssets/ring1-20,Scene7SharedAssets/ring1-21,Scene7SharedAssets/ring1-22,Scene7SharedAssets/ring1-23,Scene7SharedAssets/ring1-24),(Scene7SharedAssets/ring1-01,Scene7SharedAssets/ring1-02,Scene7SharedAssets/ring1-03,Scene7SharedAssets/ring1-04,Scene7SharedAssets/ring1-05,Scene7SharedAssets/ring1-06,Scene7SharedAssets/ring1-07,Scene7SharedAssets/ring1-08,Scene7SharedAssets/ring1-09,Scene7SharedAssets/ring1-10,Scene7SharedAssets/ring1-11,Scene7SharedAssets/ring1-12))
```

單一混合媒體集參考：

```
 asset=Scene7SharedAssets/Mixed_Media_Set_Sample
```

明確的混合媒體集：

```
asset=Scene7SharedAssets/Backpack_J;;advanced_image;,Scene7SharedAssets/Frame-6;;advanced_image;,Scene7SharedAssets/Frame-2;;advanced_image;,Scene7SharedAssets/SpinSet_Sample;;spin;,Scene7SharedAssets/ImageSet-Colors-Sample;;advanced_swatchset;,Scene7SharedAssets/Glacier_Climber_640x360;Scene7SharedAssets/Glacier_Climber_640x360;video;
```

銳利化修飾元已新增至該集中的所有影像：

```
asset=Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C%3Fop_sharpen=%3D1
```

```
asset=Scene7SharedAssets/Mixed_Media_Set_Sample%3Fop_sharpen%3D1
```

```
asset=Viewers/Pluralist%3Fop_sharpen%3D1
```
