---
title: CarouselView.iscommand
description: CarouselView.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 848eaed7-c150-4537-96a4-f2614162d58f
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 8%

---

# CarouselView.iscommand{#carouselview-iscommand}

` [CarouselView.|<containerId>_carouselView.]iscommand= *`是命令`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> iscommand（iscommand命令） </span></span> </p> </td> 
   <td colname="col2"> <p> 應用於橫幅影像的「影像服務」命令字串。 如果在URL中指定，則 <span class="codeph"> &amp;</span> 和 <span class="codeph"> =</span> 必須是HTTP編碼為 <span class="codeph"> %26</span> 和 <span class="codeph"> %3D</span>的下界。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選擇性.

## 預設 {#section-71fb773f814649b2885aefee68073641}

無。

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

在查看器URL中指定時：

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

在配置資料中指定時：

`iscommand=op_sharpen=1&op_colorize=0xff0000`
