---
title: op_brightness
description: 調整亮度。 減少或增加影像亮度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 390ed812-87ae-41e7-8021-65dd95915ae8
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 2%

---

# op_brightness{#op-brightness}

調整亮度。 減少或增加影像亮度。

`op_brightness= *`調整`*`

<table id="simpletable_2B5DB95B1FF044C8BD226D4F8311E806"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 調整</span> </p> </td> 
  <td class="stentry"> <p>亮度調整(-100...+100 int)。 </p></td> 
 </tr> 
</table>

## 屬性 {#section-c7e757f63b2c4b5ebaacbadb51c72ce4}

圖層指令。 套用至目前圖層或複合影像，如果 `layer=comp`. 被效果圖層忽略。 CMYK影像或圖層會在套用作業之前轉換為RGB。

## 預設 {#section-be56be0759634c79b4f264f194a94dbc}

`op_brightness=0`，不會變更亮度。

## 範例 {#section-c25f952f1b77409abb9ccf885862d75c}

稍微使影像的背景變暗，以強調前景內容：

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_brightness=-10&layer=1&src=myRootId/myImageId`
