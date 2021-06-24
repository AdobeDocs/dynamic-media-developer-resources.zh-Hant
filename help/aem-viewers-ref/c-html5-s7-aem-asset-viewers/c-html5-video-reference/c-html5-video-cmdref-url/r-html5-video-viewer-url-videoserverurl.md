---
description: 視訊檢視器的URL命令。
solution: Experience Manager
title: videoServerUrl
feature: Dynamic Media Classic，檢視器， SDK/API，影片
role: Developer,Business Practitioner
exl-id: 945c32e0-a67b-4c27-b661-26510615d757
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 6%

---

# videoServerUrl{#videoserverurl}

視訊檢視器的URL命令。

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
