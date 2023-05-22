---
title: ControlBar.transition
description: Carousel Viewer的配置屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 260a1767-e49a-46e3-9c3d-23efa5c3228e
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 3%

---

# ControlBar.transition{#controlbar-transition}

Carousel Viewer的配置屬性。

` [ControlBar.|<containerId>_controlBar.]transition=none|fade[, *`延遲隱藏`*[, *`持續時間`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 無|淡入</span> </p> </td> 
   <td colname="col2"> <p> 指定用於顯示或隱藏控制欄及其內容的效果類型。 </p> <p>設定為 <span class="codeph"> 無</span> 即時顯示/隱藏。 </p> <p>設定為 <span class="codeph"> 淡</span> 提供漸進漸入/漸出效果。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 延遲隱藏</span></span> </p> </td> 
   <td colname="col2"> <p> 指定由控制欄註冊的上次滑鼠/觸摸事件與時間控制欄隱藏之間的時間（秒）。 </p> <p>如果設定為 <span class="codeph"> -1</span> 元件從不觸發其自動隱藏效果，因此始終在螢幕上保持可見。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 時段</span></span> </p> </td> 
   <td colname="col2"> <p> 設定淡入/淡出動畫的持續時間（秒）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選擇性. 在禁用控制欄自動隱藏的觸摸設備上，將忽略此命令。

## 預設 {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.3`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```
