---
title: FXG伺服器通訊協定
description: 若要操作圖形，您可以使用類似指南針點的參照點。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 57d9ba37-819e-455f-9b22-bd7aabffe007
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 18%

---

# FXG伺服器通訊協定{#fxg-server-protocol}

若要操作圖形，您可以使用類似指南針點的參照點。

使用參照點，您可以相對於某個特定參照點旋轉、縮放或調整圖形的大小。參考點為`northWest`、`north`、`northEast`、`west`、`center`、`east`、`southWest`、`south`和`southeast`。 例如，使用中心參照點可將圖形中心旋轉45°。 下圖顯示參考點所在的位置、圖形、圖形從其`northWest`參考點旋轉20°，以及圖形從其`east`參考點旋轉20°。

![參考點影像](assets/wp_ref_points.png)

* A.參考點位置
* B.圖形
* C.圖形從其`northWest`參考點旋轉20度
* D.圖形從其`east`參考點旋轉20度

語法如下：

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

預設值為none。 `inherit`值會將`s7:referencePoint`值（如果不是`none`）從頁面或群組層級的頂端傳給所有子項。 `none`設定表示物件沒有參考點，且使用FXG座標系。

>[!NOTE]
>
>若要使用參照點，並且該物件在處理之後不包含任何置換，請在處理該物件之後更新它的 x 和 y 值。

當來自`s7:referencePoint`的值用於群組（或路徑、線條元素或沒有明確寬度和高度定義的元素）時，該值會套用至群組的累積邊界方框。 例如，群組中所有物件之邊界方框的左上角做為群組的`northWest`參考點；右下角做為群組的`southEast`參考點。
