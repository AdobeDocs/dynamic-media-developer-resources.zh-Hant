---
description: 配置元件在調整大小期間如何為主視圖和彈出視圖獲取新映像。
solution: Experience Manager
title: FlyoutZoomView.imagereload
feature: Dynamic Media Classic，檢視器，SDK/API，混合媒體集
role: Developer,Business Practitioner
exl-id: 1bb57c89-4ceb-40d6-8054-d51c1573431c
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 3%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

配置元件在調整大小期間如何為主視圖和彈出視圖獲取新映像。

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *``*[; *`widthwidth`*]]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p>設為<span class="codeph"> 0 </span>時，元件在調整大小期間不會載入新影像，且彈出檢視中的影像解析度不會變更。 </p> <p>當設定為<span class="codeph"> 1 </span>時，可以指定載入到主視圖中的影像的一個或多個寬度斷點。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 斷點， <span class="varname"> 寬度 </span>[; <span class="varname"> width  </span>]  </span> </p> </td> 
   <td colname="col2"> <p>載入到主視圖的影像的寬度斷點。 元件將始終使用最適的初始載入大小。 調整大小後，將確保主視圖中的影像始終以等於最大斷點的寬度下載，並在客戶端上縮小。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`imagereload=1,breakpoint,200;400;800;1600`
