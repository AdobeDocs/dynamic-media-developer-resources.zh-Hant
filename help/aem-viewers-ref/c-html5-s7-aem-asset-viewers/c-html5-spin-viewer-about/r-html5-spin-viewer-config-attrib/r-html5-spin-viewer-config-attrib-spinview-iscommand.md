---
title: SpinView.iscommand
description: SpinView.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 6924e133-31f4-4c00-8bcc-25749b52a68d
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 8%

---

# SpinView.iscommand{#spinview-iscommand}

` [SpinView.|<containerId>_spinView.]iscommand= *`是命令`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> iscommand（iscommand命令）</span></span> </p> </td> 
   <td colname="col2"> <p> 應用於旋轉影像的「影像服務」命令字串。 如果在URL中指定，則 <span class="codeph"> &amp;</span> 和 <span class="codeph"> =</span> 必須是HTTP編碼為 <span class="codeph"> %26</span> 和 <span class="codeph"> %3D</span>的下界。 </p> <p> <p>注：不支援影像大小調整操作命令。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-924163cb2f6542499f49894becef7fb5}

選填。

## 預設 {#section-7a2128fd488941948aff18421f533ccf}

無。

## 範例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

在查看器URL中指定時：

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

在配置資料中指定時：

`iscommand=op_sharpen=1&op_colorize=0xff0000`
