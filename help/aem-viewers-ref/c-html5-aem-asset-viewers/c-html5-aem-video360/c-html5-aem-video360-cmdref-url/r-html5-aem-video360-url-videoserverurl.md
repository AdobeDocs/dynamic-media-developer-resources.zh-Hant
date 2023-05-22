---
title: 視頻伺服器URL
description: Video360 Viewer的URL命令。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 76204d0a-449b-4fe5-a2aa-36739fab482f
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '51'
ht-degree: 5%

---

# 視頻伺服器URL{#videoserverurl}

Video360 Viewer的URL命令。

` videoServerUrl= *`視頻根路徑`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 視頻根路徑</span> </span> </p> </td> 
   <td colname="col2"> <p> 視頻伺服器根路徑。 如果未指定域，則將應用從中提供頁面的域。 應用標準URI路徑解析。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選擇性. 標準SaaS使用不需要。

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

`/is/content/`

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
videoServerUrl=http://s7d9.scene7.com/is/content/
```
