---
description: 調整亮度。 降低或增加影像亮度。
solution: Experience Manager
title: op_brightness
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 390ed812-87ae-41e7-8021-65dd95915ae8
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '80'
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

圖層命令。 若`layer=comp`，則套用至目前層或複合影像。 被效果層忽略。 在應用操作之前， CMYK影像或圖層會轉換為RGB。

## 預設 {#section-be56be0759634c79b4f264f194a94dbc}

`op_brightness=0`，不會改變亮度。

## 範例 {#section-c25f952f1b77409abb9ccf885862d75c}

稍微拖曳影像背景以強調前景內容：

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_brightness=-10&layer=1&src=myRootId/myImageId`
