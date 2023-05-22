---
title: 互動式資料
description: Interactive Video Viewer的URL命令。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: f9f5aa7a-3e0a-434a-8623-b439c9b6f18b
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 5%

---

# 互動式資料{#interactivedata}

Interactive Video Viewer的URL命令。

`interactivedata= *`file`*`

互動式資料將視頻內容中的某些時間區域與產品資料相關聯，產品資料稍後顯示在視頻旁邊的互動式色板中。 它還與視頻播放結束時顯示的行動要求面板相關聯。 它還提供了在「行動呼叫」面板中顯示的互動式視頻的標題。

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 檔案</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定WebVTT交互資料內容的URL或路徑。 WebVTT檔案必須由影像服務提供。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選擇性.

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

無。

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
interactivedata=is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt
```
