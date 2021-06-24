---
description: 視訊時間是數值顯示，可顯示目前播放視訊的目前時間和持續時間。
solution: Experience Manager
title: 視訊時間
feature: Dynamic Media Classic，檢視器， SDK/API，互動式影片
role: Developer,Business Practitioner
exl-id: 90ec189e-6de4-44b3-8760-1e8636b919ba
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 2%

---

# 視訊時間{#video-time}

視訊時間是數值顯示，可顯示目前播放視訊的目前時間和持續時間。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

視訊時間字型系列、字型大小和字型顏色是CSS可控制的屬性之一。 它也可由CSS相對於包含它的控制列進行定位。

視訊時間的外觀是透過下列CSS類別選取器控制：

```
.s7interactivevideoviewer .s7videotime
```

## 視訊時間的CSS屬性 {#css-properties-of-video-time}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 頂部 </span> </p> </td> 
   <td colname="col2"> <p>從上邊框的位置，包括邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右側 </span> </p> </td> 
   <td colname="col2"> <p>從右邊框定位，包括邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 視訊時間控制的寬度。 Internet Explorer 8或更高版本需要此屬性才能正常工作。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型系列  </span> </p> </td> 
   <td colname="col2"> <p>用於時間顯示文本的字型系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型大小  </span> </p> </td> 
   <td colname="col2"> <p>用於時間顯示文本的字型大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>用於時間顯示文本的字型顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 範例 {#section-e8caea0a303c425a8a637c2a47c06355}

將視頻時間設定為淺灰色（十六進位`#BBBBBB`），大小為12像素，從控制條的頂部定位15像素，從控制條的上邊緣和右邊緣設定80像素。

```
.s7interactivevideoviewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```
