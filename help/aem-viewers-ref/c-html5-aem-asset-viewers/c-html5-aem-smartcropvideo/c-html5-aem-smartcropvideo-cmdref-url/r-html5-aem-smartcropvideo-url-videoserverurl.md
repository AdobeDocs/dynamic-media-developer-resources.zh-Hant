---
title: videoServerUrl
description: 智慧型裁切視訊檢視器的URL命令。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 7%

---

# videoServerUrl{#videoserverurl}

智慧型裁切視訊檢視器的URL命令。

` videoServerUrl= *`videoRootPath`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> videoRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p> 視訊伺服器根路徑。 若未指定網域，則會改為套用提供頁面的網域。 標準URI路徑解析度適用。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選填。標準SaaS使用不需要。

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

`/is/content/`

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
videoServerUrl=http://s7d1.scene7.com/is/content/
```
