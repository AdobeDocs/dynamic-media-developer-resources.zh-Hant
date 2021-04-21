---
description: 配置元件在調整大小期間如何為主視圖和彈出視圖讀取新影像。
solution: Experience Manager
title: FlyoutZoomView.imagereload
feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 3%

---


# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

配置元件在調整大小期間如何為主視圖和彈出視圖讀取新影像。

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`寬`*[; *`度`*]]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p>設為<span class="codeph"> 0 </span>時，元件在調整大小時不會載入新影像，而彈出檢視中的影像解析度也不會變更。 </p> <p>當設為<span class="codeph"> 1 </span>時，可讓您為載入主檢視的影像指定一個或多個寬度中斷點。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 斷點， <span class="varname"> 寬度 </span>[; <span class="varname"> 寬度 </span>]  </span> </p> </td> 
   <td colname="col2"> <p>載入主檢視中之影像的寬度中斷點。 元件將始終使用最適合初始載荷的大小。 調整大小後，可確保主視圖中的影像始終以等於最接近較大斷點的寬度下載，並在客戶端上縮小。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`imagereload=1,breakpoint,200;400;800;1600`
