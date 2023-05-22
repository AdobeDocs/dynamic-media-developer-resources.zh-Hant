---
title: ControlBar.transition
description: 指定用於顯示或隱藏控制欄及其內容的效果類型。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: abe8affb-cbcd-4072-b2ed-91a398b1d678
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`延遲隱藏`*[, *`持續時間`*]`

<table id="table_F71AA834FE494949A2D4B569EA5E721F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 無|淡入 </span> </p> </td> 
   <td colname="col2"> <p> 指定用於顯示或隱藏控制欄及其內容的效果類型。 使用 <span class="codeph"> 無 </span> 即時展示和隱藏； <span class="codeph"> 淡 </span> 提供漸入漸出效果（Internet Explorer 8不支援）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 延遲隱藏 </span> </span> </p> </td> 
   <td colname="col2"> <p> 指定控制欄所登記的上次滑鼠/觸摸事件與時間控制欄的隱藏之間的時間（秒）。 </p> <p> 如果設定為 <span class="codeph"> -1 </span>，元件從不觸發其自動隱藏效果，並始終在螢幕上保持可見。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 持續時間 </span> </span> </p> </td> 
   <td colname="col2"> <p> 設定淡入淡出動畫的持續時間（秒）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選擇性. 在觸摸設備上，此命令被忽略，其中禁用了控制欄自動隱藏。

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

`fade,2,0.5`

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`transition=none`
