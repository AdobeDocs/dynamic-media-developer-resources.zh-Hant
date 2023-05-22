---
description: 調整亮度。 降低或增加影像亮度。
solution: Experience Manager
title: op_brightness
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 390ed812-87ae-41e7-8021-65dd95915ae8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 2%

---

# op_brightness{#op-brightness}

調整亮度。 降低或增加影像亮度。

`op_brightness= *`阿傑`*`

<table id="simpletable_2B5DB95B1FF044C8BD226D4F8311E806"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 阿傑</span> </p> </td> 
  <td class="stentry"> <p>亮度調整(-100..+100 int)。 </p></td> 
 </tr> 
</table>

## 屬性 {#section-c7e757f63b2c4b5ebaacbadb51c72ce4}

層命令。 應用於當前圖層或複合影像 `layer=comp`。 被效果層忽略。 在應用操作之前，CMYK影像或圖層將轉換為RGB。

## 預設 {#section-be56be0759634c79b4f264f194a94dbc}

`op_brightness=0`，以保持亮度不變。

## 範例 {#section-c25f952f1b77409abb9ccf885862d75c}

稍加縮放影像背景以強調前景內容：

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_brightness=-10&layer=1&src=myRootId/myImageId`
