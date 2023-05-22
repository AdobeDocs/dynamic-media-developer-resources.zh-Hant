---
title: 示例C
description: 建立「紙娃娃」分層應用程式。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 70232055-2a4c-4e56-8076-3cd56a9004c5
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# 示例C{#example-c}

建立「紙娃娃」分層應用程式。

背景影像包含模型或人體模型的照片。 影像目錄中的其他記錄包含各種服裝和附件，這些物品被拍攝以匹配形狀和大小的人體模型。

每個服裝/附件照片被蒙版並裁切到蒙版邊界框以最小化影像尺寸。 小心地控制影像錨點和解析度以保持圖層和背景影像之間的對齊，並且所有影像都被添加到影像目錄中，並將適當的值儲存在 `catalog::Resolution` 和 `catalog::Anchor`。

除分層外，還要更改選定項的顏色。 對這些項的記錄進行預處理以去除原始顏色並以適合彩色化命令的方式調節亮度和對比度。 此預處理可能是離線完成的，使用像Adobe Photoshop這樣的影像編輯工具，或者在簡單情況下，可以通過添加 `op_brightness=` 和 `op_contrast=` 到 `catalog::Modifier`的子菜單。

此應用程式不需要單獨的模板，因為所有對象都已通過其影像錨點正確對齊( `catalog::Anchor`)和縮放( `catalog::Resolution`)。 由客戶端負責，以確保適當的層順序。

典型的請求可能如下所示：

```
http://server/rootId/mannequin?&hei=400&qlt=90&
layer=1&res=999&src=rootId/tankTopGeneric&colorize=240,122,17&
 layer=2&res=999&src=rootId/skirt14a&
layer=3&res=999&src=rootId/jacket09&
layer=4&res=999&src=rootId/hat2generic&colorize=12,15,34&
 layer=5&res=999&src=rootId/sunglasses&
layer=6&res=999&src=rootId/shoes21
```

只指定高度。 這樣，返回的影像就可以根據人體模型影像的長寬比而在寬度上變化，而不會得到用背景顏色填充的邊距。

只要每個層都相同，就不應該指定什麼解析度。 此版本不允許視圖大於複合影像。 指定大解析度值可避免與此限制相關的問題。 所有處理和合成都以所請求的影像大小的最佳解析度完成，以幫助獲得最佳效能和輸出質量。

的 `res=` 如果所有源影像的解析度都完全相同（這種應用程式很可能是這種情況），則可省略命令。

的 `rootId` 必須為所有 `src=` 命令，即使它們與 `rootId` 在url路徑中指定。

如果不使用影像目錄，則無法採用基於解析度的縮放方法。 在這種情況下，必鬚根據每個層項的比例，為每個層項計算顯式比例因子 `catalog::Resolution` 每個層的值 `catalog::Resolution` 後台層的值。 因此，複合請求（層數較少）可能如下所示：

```
http://server/myApp/mannequin.tif?&hei=400&qlt=90&
 layer= 1&scale=0.3423&anchor=345,225&src=myApp/images/tankTopGeneric.tif&colorize=240,122,17&
 layer=2&scale=0.8544&anchor=140,-157&src=myApp/images/skirt14a
```
