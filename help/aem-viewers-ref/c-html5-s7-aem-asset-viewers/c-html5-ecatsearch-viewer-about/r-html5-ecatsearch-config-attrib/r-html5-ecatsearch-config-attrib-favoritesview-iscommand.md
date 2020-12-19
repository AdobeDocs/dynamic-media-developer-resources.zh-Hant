---
description: 套用至所有縮圖的「影像伺服」命令字串。
seo-description: 套用至所有縮圖的「影像伺服」命令字串。
seo-title: FavoritesView.iscommand
solution: Experience Manager
title: FavoritesView.iscommand
topic: Dynamic media
uuid: be3d49d1-d5d2-4ecd-bc8f-fe5f80204c76
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 7%

---


# FavoritesView.iscommand{#favoritesview-iscommand}

套用至所有縮圖的「影像伺服」命令字串。

[!DNL `[FavoritesView.|<containerId>_favoritesView.]iscommand= *`isCommand`*`]

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> 如果在URL中指定，所有<span class="codeph"> &amp;</span>和<span class="codeph"> =</span>的出現次數都必須分別以HTTP編碼為<span class="codeph"> %26</span>和<span class="codeph"> %3D</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選填。

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

無。

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

在檢視器URL中指定時。

[!DNL `iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`]

在配置資料中指定時。

[!DNL `iscommand=op_sharpen=1&op_colorize=0xff0000`]
