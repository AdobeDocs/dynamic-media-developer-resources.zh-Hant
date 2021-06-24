---
description: 建立「紙娃娃」分層應用程式。
solution: Experience Manager
title: 範例C
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 70232055-2a4c-4e56-8076-3cd56a9004c5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# 範例C{#example-c}

建立「紙娃娃」分層應用程式。

背景影像包含模型或人體模型的照片。 影像目錄中的其他記錄包含各種服裝和配飾項目，拍攝這些記錄是為了在形狀和大小上匹配人體模型。

每個服裝/配飾像片都被遮罩並裁切至遮罩邊界方框，以將影像大小減至最小。 小心地控制影像錨點和解析度以保持圖層和背景影像之間的對齊，並且所有影像都被添加到影像目錄中，並將適當的值儲存在`catalog::Resolution`和`catalog::Anchor`中。

除了分層，我們還要更改所選項目的顏色。 對這些項的記錄進行預處理，以去除原始顏色並以適合著色命令的方式調整亮度和對比度。 此預處理作業可以離線完成，使用影像編輯工具(例如Photoshop)，或在簡單情況下，可透過將`op_brightness=`和`op_contrast=`新增至`catalog::Modifier`欄位來逐步完成。

此應用程式不需要單獨的模板，因為所有對象已通過其影像錨點(`catalog::Anchor`)和縮放(`catalog::Resolution`)正確對齊。 由用戶端自行決定，以確保適當的層順序。

一般要求可能如下所示：

```
http://server/rootId/mannequin?&hei=400&qlt=90&
layer=1&res=999&src=rootId/tankTopGeneric&colorize=240,122,17&
 layer=2&res=999&src=rootId/skirt14a&
layer=3&res=999&src=rootId/jacket09&
layer=4&res=999&src=rootId/hat2generic&colorize=12,15,34&
 layer=5&res=999&src=rootId/sunglasses&
layer=6&res=999&src=rootId/shoes21
```

僅指定高度。 這允許返回的影像根據人體模型影像的長寬比而在寬度上變化，而不會得到用背景顏色填充的邊距。

只要每個層都相同，為每個層指定的解析度都不重要。 此版本不允許檢視大於複合影像。 指定大解析度值可避免與此限制相關的問題。 所有處理和合成都以所請求的影像大小的最佳解析度完成，以幫助實現最佳效能和輸出質量。

如果所有源影像的全尺寸解析度相同（這很可能是此類應用程式的情況），則可以忽略`res=`命令。

必須為所有`src=`命令指定`rootId`，即使它們與url路徑中指定的`rootId`相同。

如果不使用影像目錄，則無法使用基於解析度的縮放方法。 在這種情況下，必鬚根據每個層的`catalog::Resolution`值與背景層的`catalog::Resolution`值的比率，為每個層項計算顯式縮放因子。 因此，複合請求（層數較少）可能如下所示：

```
http://server/myApp/mannequin.tif?&hei=400&qlt=90&
 layer= 1&scale=0.3423&anchor=345,225&src=myApp/images/tankTopGeneric.tif&colorize=240,122,17&
 layer=2&scale=0.8544&anchor=140,-157&src=myApp/images/skirt14a
```
