---
title: ControlBar.transition
description: 互動式視訊檢視器的設定屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: a8bb32b4-0fd9-4887-98ef-31c3426092b6
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 4%

---

# ControlBar.transition{#controlbar-transition}

互動式視訊檢視器的設定屬性。

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`delaytohideduration`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 無|淡出</span> </p> </td> 
   <td colname="col2"> <p> 指定用於顯示/隱藏控制欄及其內容的效果類型。 </p> <p>若為即時顯示/隱藏，則設為<span class="codeph"> none</span>。 </p> <p>設為<span class="codeph"> fade</span>以提供漸進淡入/淡出效果。 Internet Explorer 8不支援。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delayhide</span></span> </p> </td> 
   <td colname="col2"> <p> 指定控制欄註冊的上次滑鼠/觸控事件與時間控制欄隱藏之間的秒數。 如果設為<span class="codeph"> -1</span>，元件永遠不會觸發其自動隱藏效果，因此一律會顯示在畫面上。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 時段</span></span> </p> </td> 
   <td colname="col2"> <p> 設定淡入/淡出動畫的持續時間（以秒為單位）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選填。

## 預設 {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.5`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```
