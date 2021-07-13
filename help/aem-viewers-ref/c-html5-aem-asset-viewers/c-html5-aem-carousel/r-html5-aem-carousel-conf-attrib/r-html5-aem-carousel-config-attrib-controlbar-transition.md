---
description: 輪播檢視器的設定屬性。
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media Classic，檢視器，SDK/API，輪播橫幅
role: Developer,User
exl-id: 260a1767-e49a-46e3-9c3d-23efa5c3228e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 3%

---

# ControlBar.transition{#controlbar-transition}

輪播檢視器的設定屬性。

` [ControlBar.|<containerId>_controlBar.]transition=none|fade[, *``*[, *`delaytohideduration`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 無|淡出</span> </p> </td> 
   <td colname="col2"> <p> 指定用於顯示或隱藏控制欄及其內容的效果類型。 </p> <p>若為即時顯示/隱藏，則設為<span class="codeph"> none</span>。 </p> <p>設為<span class="codeph"> fade</span>以提供漸進淡入/淡出效果。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delayhide</span></span> </p> </td> 
   <td colname="col2"> <p> 指定控制欄註冊的上次滑鼠/觸控事件與時間控制欄隱藏之間的秒數。 </p> <p>如果設為<span class="codeph"> -1</span>，元件永遠不會觸發其自動隱藏效果，因此一律會顯示在畫面上。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 時段</span></span> </p> </td> 
   <td colname="col2"> <p> 設定淡入/淡出動畫的持續時間（以秒為單位）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選填。在禁用控制欄自動隱藏的觸摸設備上，會忽略此命令。

## 預設 {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.3`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```
