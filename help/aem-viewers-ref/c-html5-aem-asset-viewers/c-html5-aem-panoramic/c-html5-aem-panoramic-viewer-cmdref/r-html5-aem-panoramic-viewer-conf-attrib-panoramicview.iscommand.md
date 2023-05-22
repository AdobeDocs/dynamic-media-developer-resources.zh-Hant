---
title: PanoramicView.iscommand
description: 全景查看器的配置屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: dfd80e5727a128f272855f1f28e1bc89cb2436bf
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 4%

---

# PanoramicView.iscommand{#panoramicview-iscommand}

全景查看器的配置屬性。

` [PanoramicView.|<containerId>_panoramicView.]iscommand=isCommand `

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 是命令</span> </span> </p> </td> 
   <td colname="col2"> <p> 應用於影像的「影像服務」命令字串。  如果在URL中指定，請確保HTTP編碼所有出現的 <span class="codeph"> &amp;</span> 和 <span class="codeph"> =</span> 如 <span class="codeph"> %26</span> 和 <span class="codeph"> %3D</span>的下界。 </p> </td> 
  </tr> 
 </tbody> 
</table>


## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選擇性.

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

無預設值。

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

在查看器URL中指定時。

```
iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000
```

在配置資料中指定時。

```
iscommand=op_sharpen=1&op_colorize=0xff0000
```
