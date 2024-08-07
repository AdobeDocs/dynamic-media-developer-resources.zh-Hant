---
title: 視訊時間
description: 視訊時間是顯示目前播放視訊之目前時間和持續時間的數值顯示。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 78657fd2-e805-4047-be0a-592143025986
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%

---

# 視訊時間{#video-time}

視訊時間是顯示目前播放視訊之目前時間和持續時間的數值顯示。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

視訊時間字型系列、字型大小和字型顏色是CSS可以控制的屬性。 您也可以透過CSS將其放置到相對於包含它的控制列的位置。

視訊時間的外觀可透過下列CSS類別選取器控制：

```
.s7video360viewer .s7videotime
```

## 視訊時間的CSS屬性 {#css-properties-of-video-time}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">前</span> </p> </td> 
   <td colname="col2"> <p>上邊框的位置，包括邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">右</span> </p> </td> 
   <td colname="col2"> <p>從右邊框定位，包括內距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">寬度</span> </p> </td> 
   <td colname="col2"> <p> 視訊時間控制項的寬度。 Internet Explorer 8或更新版本需要此屬性才能正常運作。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字型系列</span> </p> </td> 
   <td colname="col2"> <p>用於時間顯示文字的字型系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字型大小</span> </p> </td> 
   <td colname="col2"> <p>用於時間顯示文字的字型大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">色彩</span> </p> </td> 
   <td colname="col2"> <p>用於時間顯示文字的字型顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**範例** — 將視訊時間設為淺灰色（十六進位`#BBBBBB`），大小為12畫素，位置為控制列頂端的15畫素，以及控制列頂端與右邊緣的80畫素。

```
.s7video360viewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```
