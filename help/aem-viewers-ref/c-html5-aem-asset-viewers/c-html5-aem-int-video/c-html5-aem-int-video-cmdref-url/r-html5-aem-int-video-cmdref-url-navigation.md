---
description: 互動式視訊檢視器的URL命令。
solution: Experience Manager
title: 導覽
feature: Dynamic Media Classic，檢視器， SDK/API，互動式影片
role: Developer,Business Practitioner
exl-id: 9852e723-fd1f-4ade-921b-cfb92bf9f2ad
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 12%

---

# 導覽{#navigation}

互動式視訊檢視器的URL命令。

` navigation= *`file`*`

檢視器支援透過托管WebVTT檔案進行視訊章節導覽。 不支援提示定位操作器。

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 檔案</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定WebVTT導航內容的URL或路徑。 影像伺服器應托管WebVTT檔案。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選填。

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

無。

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
navigation=is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.navigation.vtt,1
```
