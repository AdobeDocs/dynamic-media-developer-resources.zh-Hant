---
description: 若要處理圖形，您可以使用參照點 (類似於方位點)。
solution: Experience Manager
title: FXG伺服器協定
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 57d9ba37-819e-455f-9b22-bd7aabffe007
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 85%

---

# FXG伺服器協定{#fxg-server-protocol}

若要處理圖形，您可以使用參照點 (類似於方位點)。

使用參照點，您可以相對於某個特定參照點旋轉、縮放或調整圖形的大小。參考點為`northWest`、`north`、`northEast`、`west`、`center`、`east`、`southWest`、`south`和`southeast`。 例如，透過使用 center 參照點，您可以將一個圖形繞其中心旋轉 45 度。下圖顯示參照點的位置、一個圖形、該圖形從其 `northWest` 參照點旋轉 20 度所得到的圖形和從其 `east` 參照點旋轉 20 度所得到的圖形。

![](assets/wp_ref_points.png)

* A.參考點位置
* B.圖
* C.圖形從其`northWest`參考點旋轉了20度
* D.圖形從其`east`參考點旋轉了20度

語法如下：

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

預設值為 none。`inherit` 值將 `s7:referencePoint` 值從頁面頂部或群組層級傳遞到所有子項，但前提是它未設為 `none`。`none` 設定表示該物件沒有參照點，而使用 FXG 座標系統。

>[!NOTE]
>
>若要使用參照點，並且該物件在處理之後不包含任何置換，請在處理該物件之後更新它的 x 和 y 值。

當`s7:referencePoint` 的值與群組 (或路徑、線條元素或任何沒有明確定義寬度和高度的元素) 一起使用時，該值將套用於該群組的累積邊界方框。例如，該群組中所有物件的邊界框左上方的點作為該群組的 `northWest` 參照點；右下方的點作為 `southEast` 參照點。
