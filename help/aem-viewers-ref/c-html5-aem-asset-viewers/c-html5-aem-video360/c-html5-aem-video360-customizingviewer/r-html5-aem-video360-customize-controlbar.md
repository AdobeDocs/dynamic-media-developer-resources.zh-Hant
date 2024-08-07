---
title: 控制列
description: 控制列是矩形的區域，其中包含並位於所有可用於視訊檢視器的使用者介面控制項後面，例如播放/暫停按鈕和音量控制項。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 06078310-8aeb-449f-919a-ce88ddc8c4b3
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---

# 控制列{#control-bar}

控制列是矩形的區域，其中包含並位於所有可用於視訊檢視器的使用者介面控制項後面，例如播放/暫停按鈕和音量控制項。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

控制列一律採用完整的可用檢視器寬度。 您可以透過CSS變更其相對於視訊檢視器容器的顏色、高度和垂直位置。

下列CSS類別選取器會控制控制列的外觀：

```
.s7video360viewer .s7controlbar
```

## 控制列的CSS屬性 {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">前</span> </p> </td> 
   <td colname="col2"> <p>上邊框的位置，包括邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">後</span> </p> </td> 
   <td colname="col2"> <p> 從下邊框定位，包括內距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>控制列的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色彩</span> </p> </td> 
   <td colname="col2"> <p>控制列的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**範例** — 以灰色控制列設定視訊檢視器，該控制列高度為30畫素，位於視訊檢視器容器的頂端。

```
.s7video360viewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
