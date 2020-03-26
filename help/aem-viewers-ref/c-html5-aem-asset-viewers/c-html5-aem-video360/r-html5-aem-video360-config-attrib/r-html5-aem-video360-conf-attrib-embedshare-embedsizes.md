---
description: Video360檢視器的設定屬性。
seo-description: Video360檢視器的設定屬性。
seo-title: EmbedShare.embedsizes
solution: Experience Manager
title: EmbedShare.embedsizes
topic: Dynamic media
uuid: d3eea508-fb1e-4147-b853-a16f51725dd7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# EmbedShare.embedsizes{#embedshare-embedsizes}

Video360檢視器的設定屬性。

` [EmbedShare.|<containerId>_embedShare.]embedsizes= *`寬高`*, *``*[,0|1][; *``*, *`寬高`*[,0|1]]`

在內嵌共用模式對話方塊中，指定大小組合方塊的內嵌大小清單。

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
   <td colname="col2"> <p> 指定是否應在組合框中初始預選此清單項。 </p> </td> 
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

