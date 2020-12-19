---
description: 調整亮度。 降低或增加影像亮度。
seo-description: 調整亮度。 降低或增加影像亮度。
seo-title: op_brightness
solution: Experience Manager
title: op_brightness
topic: Scene7 Image Serving - Image Rendering API
uuid: 751ec9e5-4a70-438d-950c-deff4db034b1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 3%

---


# op_brightness{#op-brightness}

調整亮度。 降低或增加影像亮度。

`op_brightness= *`adj`*`

<table id="simpletable_2B5DB95B1FF044C8BD226D4F8311E806"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>亮度調整(-100...+100 int)。 </p></td> 
 </tr> 
</table>

## 屬性 {#section-c7e757f63b2c4b5ebaacbadb51c72ce4}

圖層命令。 如果`layer=comp`，則套用至目前圖層或複合影像。 被效果圖層忽略。 在應用操作之前，CMYK影像或圖層將轉換為RGB。

## 預設 {#section-be56be0759634c79b4f264f194a94dbc}

`op_brightness=0`，不會改變亮度。

## 範例 {#section-c25f952f1b77409abb9ccf885862d75c}

稍微加深影像的背景以強調前景內容：

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_brightness=-10&layer=1&src=myRootId/myImageId`
