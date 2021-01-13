---
description: SpinView.enableHD
solution: Experience Manager
title: SpinView.enableHD
topic: Dynamic media
uuid: 3e7cdb44-4366-4e84-a6c7-c1cf1f5e6344
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 7%

---


# SpinView.enableHD{#spinview-enablehd}

` [SpinView.|<containerId>_spinView.]enableHD=always|never|limit[, *`數字`*]`

<table id="table_8929B59833DE4E1C89FA4BCF07309809"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> 對<span class="codeph"> devicePixelRatio</span>大於<span class="codeph"> 1</span>的裝置啟用、限制或停用最佳化，即具有高密度顯示（例如iPhone4和類似裝置）的裝置。 如果處於活動狀態，則元件將限制IS影像請求的大小，就好像設備只有<span class="codeph"> 1</span>的像素比，因此減少了頻寬。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 數字</span></span> </p> </td> 
   <td colname="col2"> <p> 如果使用<span class="codeph"> limit</span>設定，元件僅會啟用高像素密度，而達到指定的限制。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`limit,1500`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`enableHD=always`
