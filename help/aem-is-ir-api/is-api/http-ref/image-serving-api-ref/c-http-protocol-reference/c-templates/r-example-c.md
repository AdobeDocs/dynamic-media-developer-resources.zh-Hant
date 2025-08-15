---
title: 範例C
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

# 範例C{#example-c}

建立「紙娃娃」分層應用程式。

背景影像包含模型或人體模型的像片。 影像目錄中的其他記錄包含各種服裝和配件，拍攝以符合人體模型的形狀和大小。

每個服飾/配件像片都會經過遮罩，並裁切至遮罩邊界方框，以將影像大小最小化。 影像錨點和解析度會經過謹慎控制，以維持圖層與背景影像的對齊，而且所有影像都會新增至影像目錄，並將適當的值儲存於`catalog::Resolution`和`catalog::Anchor`。

除了分層外，您還需要變更所選專案的顏色。 這些專案的記錄會經過預先處理，以移除原始顏色，並以適合彩色化指令的方式調整亮度和對比。 此預先處理作業可以離線完成，使用影像編輯工具(例如Adobe Photoshop)來完成，或者在簡單的情況下，可以將`op_brightness=`和`op_contrast=`新增到`catalog::Modifier`欄位來逐一完成。

此應用程式不支援個別的範本，因為所有物件已由其影像錨點( `catalog::Anchor`)正確對齊，且已縮放( `catalog::Resolution`)。 由使用者端自行決定要確保適當的圖層順序。

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

僅指定高度。 如此可讓傳回的影像依人體模型影像的外觀比例而改變寬度，而不會以背景顏色填滿邊界。

只要每個圖層都一樣，指定何種解析度就無關緊要。 此版本不允許檢視大於複合影像。 指定大型解析度值可避免與此限制相關的問題。 所有處理和合成作業都是以最佳解析度來完成，以符合要求的影像大小，進而達到最佳的效能和輸出品質。

如果所有來源影像在完整比例下都有相同的解析度（這很可能是這種應用程式的情況），則可以省略`res=`命令。

必須為所有`rootId`命令指定`src=`，即使它們與URL路徑中指定的`rootId`相同。

如果沒有要使用影像目錄，就無法使用以解析度為基礎的縮放方法。 在此情況下，必須根據每個圖層的`catalog::Resolution`值與背景圖層的`catalog::Resolution`值的比例，計算每個圖層專案的明確比例係數。 因此，合成請求（層數較少）可能如下所示：

```
http://server/myApp/mannequin.tif?&hei=400&qlt=90&
 layer= 1&scale=0.3423&anchor=345,225&src=myApp/images/tankTopGeneric.tif&colorize=240,122,17&
 layer=2&scale=0.8544&anchor=140,-157&src=myApp/images/skirt14a
```
