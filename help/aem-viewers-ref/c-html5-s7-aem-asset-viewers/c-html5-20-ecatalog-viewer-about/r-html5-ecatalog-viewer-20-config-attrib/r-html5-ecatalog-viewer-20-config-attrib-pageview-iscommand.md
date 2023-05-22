---
title: PageView.iscommand
description: PageView.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d1b05fe7-901b-4030-9b71-e4e0e5191abf
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 7%

---

# PageView.iscommand{#pageview-iscommand}

` [PageView.|<containerId>_pageView.]iscommand= *`是命令`*`

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 是命令</span></span> </p> </td> 
   <td colname="col2"> <p> 應用於頁面影像的「影像服務」命令字串。 如果在URL中指定，則 <span class="codeph"> &amp;</span> 和 <span class="codeph"> =</span> 必須是HTTP編碼為 <span class="codeph"> %26</span> 和 <span class="codeph"> %3D</span>的下界。 </p> <p> <p>注：不支援影像大小調整操作命令。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-df5a0604766b4ac2b9a6742b377e427c}

選擇性.

## 預設 {#section-9f2bf4c418e5441c9fff3eb755f7bda6}

無。

## 範例 {#section-813de2905d6c44c0991cfe0931581462}

在查看器URL中指定時。

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

在配置資料中指定時。

`iscommand=op_sharpen=1&op_colorize=0xff0000`
