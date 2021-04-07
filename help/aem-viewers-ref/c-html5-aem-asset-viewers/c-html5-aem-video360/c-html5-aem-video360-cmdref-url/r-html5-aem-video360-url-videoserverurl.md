---
description: Video360檢視器的URL命令。
solution: Experience Manager
title: videoServerUrl
feature: Dynamic Media經典，檢視器，SDK/API,360 VR視訊
role: 開發人員，商業從業人員
exl-id: 76204d0a-449b-4fe5-a2aa-36739fab482f
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 6%

---

# videoServerUrl{#videoserverurl}

Video360檢視器的URL命令。

` videoServerUrl= *`videoRootPath`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> videoRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p> 視訊伺服器根路徑。 如果未指定網域，則會改為套用從中提供頁面的網域。 套用標準URI路徑解析度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選填。標準SaaS使用不需要。

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

`/is/content/`

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
videoServerUrl=http://s7d9.scene7.com/is/content/
```
