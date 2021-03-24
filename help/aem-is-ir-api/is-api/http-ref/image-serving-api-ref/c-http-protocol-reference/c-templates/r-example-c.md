---
description: 建立「紙娃娃」分層應用程式。
solution: Experience Manager
title: 範例C
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 0%

---


# 範例C{#example-c}

建立「紙娃娃」分層應用程式。

背景影像包含模型或人體模型的像片。 影像目錄中的其他記錄包含各種服飾和配件，這些物品是為了配合人體模型的形狀和大小而拍攝的。

每張服裝／附件像片都會被遮色片和裁切至遮色片邊界方框，以將影像大小減到最小。 小心控制影像定位點和解析度，以維持圖層與背景影像之間的對齊，並且所有影像都會新增至影像目錄，並將適當的值儲存在`catalog::Resolution`和`catalog::Anchor`中。

除了分層外，我們還要更改所選項目的顏色。 對這些項目的記錄進行預處理以去除原始顏色並以適合於著色命令的方式調整亮度和對比度。 此預處理可能是離線、使用像是Photoshop的影像編輯工具，或者，在簡單的情況下，可將`op_brightness=`和`op_contrast=`新增至`catalog::Modifier`欄位，以輕鬆完成。

此應用程式不保證個別範本，因為所有物件都已透過其影像定位點(`catalog::Anchor`)和縮放(`catalog::Resolution`)正確對齊。 我們將決定權交給用戶端，以確保適當的圖層順序。

一般的要求可能如下所示：

```
http://server/rootId/mannequin?&hei=400&qlt=90&
layer=1&res=999&src=rootId/tankTopGeneric&colorize=240,122,17&
 layer=2&res=999&src=rootId/skirt14a&
layer=3&res=999&src=rootId/jacket09&
layer=4&res=999&src=rootId/hat2generic&colorize=12,15,34&
 layer=5&res=999&src=rootId/sunglasses&
layer=6&res=999&src=rootId/shoes21
```

僅指定高度。 這可讓傳回的影像視人體模型影像的長寬比而變更寬度，而不會填滿背景顏色的邊界。

只要每個圖層都相同，指定的解析度不重要。 此版本不允許檢視比合成影像大。 指定大解析度值可避免與此限制相關的問題。 所有處理和構圖都會以最佳解析度完成，以符合要求的影像大小，以協助達到最佳效能和輸出品質。

如果所有源映像的解析度都完全相同（這類應用程式可能是這樣），則可以忽略`res=`命令。

必須為所有`src=`命令指定`rootId`，即使它們與在url路徑中指定的`rootId`相同。

如果不要使用影像目錄，則無法使用基於解析度的縮放方法。 在這種情況下，必鬚根據每個圖層的`catalog::Resolution`值與背景圖層的`catalog::Resolution`值之比，為每個圖層項目計算明確的比例系數。 因此，複合請求（含較少圖層）可能如下所示：

```
http://server/myApp/mannequin.tif?&hei=400&qlt=90&
 layer= 1&scale=0.3423&anchor=345,225&src=myApp/images/tankTopGeneric.tif&colorize=240,122,17&
 layer=2&scale=0.8544&anchor=140,-157&src=myApp/images/skirt14a
```

