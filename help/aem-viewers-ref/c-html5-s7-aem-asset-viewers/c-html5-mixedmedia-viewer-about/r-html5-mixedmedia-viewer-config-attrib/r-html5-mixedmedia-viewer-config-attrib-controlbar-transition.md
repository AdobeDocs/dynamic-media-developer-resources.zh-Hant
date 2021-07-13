---
description: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media Classic，檢視器，SDK/API，混合媒體集
role: Developer,User
exl-id: c8792f02-ae15-4b47-8727-089691d5316a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 3%

---

# ControlBar.transition{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`delaytohideduration`*]`

<table id="table_76B7F064B9CD46BA86931A9C841F777B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 無|淡出</span> </p> </td> 
   <td colname="col2"> <p> 指定用於顯示或隱藏控制欄及其內容的效果類型。 </p> <p>使用<span class="codeph"> none</span>進行即時顯示和隱藏。 使用<span class="codeph">淡出</span>提供漸進淡入和淡出效果。 </p> <p>Internet Explorer 8不支援淡出。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delayhide</span> </span> </p> </td> 
   <td colname="col2"> <p>指定控制欄所登錄的上次滑鼠/觸控事件與時間控制欄隱藏之間的秒數。 </p> <p> 如果設為<span class="codeph"> -1</span>，元件永遠不會觸發其自動隱藏效果，且一律會顯示在畫面上。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 持續時間</span> </span> </p> </td> 
   <td colname="col2"> <p>設定淡入和淡出動畫的持續時間（以秒為單位）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`fade,2,0.5`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=none`
