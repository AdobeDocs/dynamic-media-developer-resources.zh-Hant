---
title: ControlBar.transition
description: ControlBar.transition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: c8792f02-ae15-4b47-8727-089691d5316a
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 3%

---

# ControlBar.transition{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`延遲隱藏`*[, *`持續時間`*]`

<table id="table_76B7F064B9CD46BA86931A9C841F777B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 無|淡入</span> </p> </td> 
   <td colname="col2"> <p> 指定用於顯示或隱藏控制欄及其內容的效果類型。 </p> <p>使用 <span class="codeph"> 無</span> 即時展示和隱藏。 使用 <span class="codeph"> 淡</span> 提供漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸。 </p> <p>Internet Explorer 8不支援淡出。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 延遲隱藏</span> </span> </p> </td> 
   <td colname="col2"> <p>指定控制欄註冊的上次滑鼠/觸摸事件與控制欄隱藏的時間之間的時間（以秒為單位）。 </p> <p> 如果設定為 <span class="codeph"> -1</span>，元件從不觸發其自動隱藏效果，並始終在螢幕上保持可見。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 持續時間</span> </span> </p> </td> 
   <td colname="col2"> <p>設定淡入淡出動畫的持續時間（秒）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`fade,2,0.5`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=none`
