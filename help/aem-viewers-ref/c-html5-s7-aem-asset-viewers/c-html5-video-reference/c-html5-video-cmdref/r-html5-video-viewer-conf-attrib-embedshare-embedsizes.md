---
description: 視訊檢視器的設定屬性。
solution: Experience Manager
title: EmbedShare.embedsizes
feature: Dynamic Media Classic，檢視器， SDK/API，影片
role: Developer,User
exl-id: cf075711-1275-4eb2-8cb6-fb2609711c7a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 10%

---

# EmbedShare.embedsizes{#embedshare-embedsizes}

視訊檢視器的設定屬性。

` [EmbedShare.|<containerId>_embedShare.]embedsizes= *``*, *``*[,0|1][; *``*, *`widthheightwidthheight`*[,0|1]]`

在內嵌共用強制回應對話方塊中，指定大小下拉式方塊的內嵌大小清單。

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td> 
   <td colname="col2"> <p> 內嵌寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> height </span> </span> </p> </td> 
   <td colname="col2"> <p>內嵌高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 指定是否應在組合框中最初預選此清單項。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選填。

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

`1280,960;640,480;320,240`

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
embedsizes=800,600;640,480,1
```
