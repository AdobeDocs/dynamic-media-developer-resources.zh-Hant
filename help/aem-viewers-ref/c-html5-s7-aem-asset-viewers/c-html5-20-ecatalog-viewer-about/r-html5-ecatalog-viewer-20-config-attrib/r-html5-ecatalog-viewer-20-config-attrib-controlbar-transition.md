---
description: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
topic: Dynamic media
uuid: e029173b-c004-4be8-b304-d6e2183314ad
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 3%

---


# ControlBar.transition{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`Delaytohideduration(`*[, *`延遲隱藏持續時間)`*]`

<table id="table_F71AA834FE494949A2D4B569EA5E721F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 無|淡化  </span> </p> </td> 
   <td colname="col2"> <p> 指定用於顯示或隱藏控制欄及其內容的效果類型。 使用<span class="codeph"> none </span>進行即時顯示和隱藏；<span class="codeph">淡化</span>提供漸進淡入和淡出效果（Internet Explorer 8不支援）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide  </span> </span> </p> </td> 
   <td colname="col2"> <p> 指定控制列在上次滑鼠／觸控事件與時間控制列隱藏之間的時間（以秒為單位）。 </p> <p> 如果設為<span class="codeph"> -1 </span>，元件不會觸發其自動隱藏效果，而且一律會在畫面上顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 持續時間  </span> </span> </p> </td> 
   <td colname="col2"> <p> 設定淡入和淡出動畫的持續時間，以秒為單位。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選填。在觸控裝置上會忽略此命令，其中會停用控制列自動隱藏。

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

`fade,2,0.5`

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`transition=none`
