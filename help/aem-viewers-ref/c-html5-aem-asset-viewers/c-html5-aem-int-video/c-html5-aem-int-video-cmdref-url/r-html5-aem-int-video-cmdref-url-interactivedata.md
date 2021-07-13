---
description: 互動式視訊檢視器的URL命令。
solution: Experience Manager
title: interactivedata
feature: Dynamic Media Classic，檢視器， SDK/API，互動式影片
role: Developer,User
exl-id: f9f5aa7a-3e0a-434a-8623-b439c9b6f18b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 5%

---

# interactivedata{#interactivedata}

互動式視訊檢視器的URL命令。

`interactivedata= *`file`*`

互動式資料會將視訊內容中的特定時間區域與產品資料建立關聯，產品資料稍後會顯示在視訊旁的互動式色票中。 它也會與視訊播放結束時顯示的動作呼叫面板相關聯。 它也提供動作呼叫面板中顯示之互動式視訊的標題。

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 檔案</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定WebVTT互動式資料內容的URL或路徑。 WebVTT檔案必須由影像伺服器提供。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選填。

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

無。

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
interactivedata=is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt
```
