---
description: SpinView.iscommand
solution: Experience Manager
title: SpinView.iscommand
feature: Dynamic Media Classic，檢視器，SDK/API，回轉集
role: Developer,Business Practitioner
exl-id: 6924e133-31f4-4c00-8bcc-25749b52a68d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 7%

---

# SpinView.iscommand{#spinview-iscommand}

` [SpinView.|<containerId>_spinView.]iscommand= *`isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> iscommand</span></span> </p> </td> 
   <td colname="col2"> <p> 套用至回轉影像的「影像伺服」命令字串。 如果在URL中指定，則所有<span class="codeph"> &amp;</span>和<span class="codeph"> =</span>的出現次數必須分別以<span class="codeph"> %26</span>和<span class="codeph"> %3D</span>進行HTTP編碼。 </p> <p> <p>注意： 不支援影像大小調整操作命令。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-924163cb2f6542499f49894becef7fb5}

選填。

## 預設 {#section-7a2128fd488941948aff18421f533ccf}

無。

## 範例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

在檢視器URL中指定時：

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

在設定資料中指定時：

`iscommand=op_sharpen=1&op_colorize=0xff0000`
