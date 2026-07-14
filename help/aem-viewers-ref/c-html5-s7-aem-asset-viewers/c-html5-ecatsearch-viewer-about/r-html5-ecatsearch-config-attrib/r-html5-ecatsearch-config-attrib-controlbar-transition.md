---
description: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 2e08a62b-9499-41f8-927b-89bed972b4eb
TQID: 'https://experienceleague.adobe.com/bcpeaqLRZ8ClN2OulOfO9ujXzz44Yb2HTmy-GyPQ8mU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 939895a2a379b02e733e48932434433bfa9663e1
workflow-type: tm+mt
source-wordcount: 121
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

[!DNL ` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`持續時間`*]`]

<table id="table_F71AA834FE494949A2D4B569EA5E721F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">無|淡化</span> </p> </td> 
   <td colname="col2"> <p> 指定用來顯示或隱藏控制列及其內容的效果型別。 使用<span class="codeph">無</span>立即顯示和隱藏；<span class="codeph">淡化</span>提供逐漸淡入和淡出效果（Internet Explorer 8不支援）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">延遲隱藏</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定控制列註冊的最後一個滑鼠/觸控事件與控制列隱藏的時間之間的秒數。 </p> <p> 如果設為<span class="codeph"> -1 </span>，元件永遠不會觸發其自動隱藏效果，並一律顯示在熒幕上。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">期間</span> </span> </p> </td> 
   <td colname="col2"> <p> 設定淡入和淡出動畫的持續時間（秒）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選擇性. 在已停用控制列自動隱藏的觸控裝置上，會忽略此指令。

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

[!DNL `fade,2,0.5`]

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `transition=none`]
