---
title: FlyoutZoomView.imagereload
description: 配置元件在調整大小期間如何為主視圖和彈出視圖提取新影像。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 1bb57c89-4ceb-40d6-8054-d51c1573431c
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 3%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

配置元件在調整大小期間如何為主視圖和彈出視圖提取新影像。

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`寬度`*[; *`寬度`*]]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p>設定為時 <span class="codeph"> 0 </span>，元件在調整大小時不會載入新影像，並且浮出視圖中的影像解析度不會更改。 </p> <p>設定為時 <span class="codeph"> 1 </span> 用於為載入到主視圖中的影像指定一個或多個寬度斷點。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 斷點， <span class="varname"> 寬度 </span>[; <span class="varname"> 寬度 </span>] </span> </p> </td> 
   <td colname="col2"> <p>載入到主視圖中的影像的寬度斷點。 元件始終對初始載荷使用最佳擬合大小。 調整大小後，它將確保在主視圖中始終下載影像的寬度等於最接近的較大斷點，並在客戶端上縮放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`imagereload=1,breakpoint,200;400;800;1600`
