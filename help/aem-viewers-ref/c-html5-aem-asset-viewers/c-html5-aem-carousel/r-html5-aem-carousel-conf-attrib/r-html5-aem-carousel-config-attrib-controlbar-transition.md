---
title: ControlBar.transition
description: 轉盤檢視器的設定屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 260a1767-e49a-46e3-9c3d-23efa5c3228e
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 1%

---

# ControlBar.transition{#controlbar-transition}

轉盤檢視器的設定屬性。

` [ControlBar.|<containerId>_controlBar.]transition=none|fade[, *`delaytohide`*[, *`持續時間`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">無|淡化</span> </p> </td> 
   <td colname="col2"> <p> 指定用來顯示或隱藏控制列及其內容的效果型別。 </p> <p>設定為<span class="codeph">無</span>以立即顯示/隱藏。 </p> <p>設定為<span class="codeph">淡化</span>以提供逐漸淡入/淡出效果。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> 指定控制列所登入的上次滑鼠/觸控事件與控制列隱藏之間的時間（秒）。 </p> <p>若設為<span class="codeph"> -1</span>，元件永遠不會觸發其自動隱藏效果，因此一律會顯示在熒幕上。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname">持續時間</span></span> </p> </td> 
   <td colname="col2"> <p> 設定淡入/淡出動畫的持續時間（秒）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選填。 在已停用控制列自動隱藏的觸控裝置上，會忽略此指令。

## 預設 {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.3`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```
