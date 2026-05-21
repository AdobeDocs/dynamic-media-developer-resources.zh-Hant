---
title: FXG伺服器通訊協定
description: 若要處理圖形，您可以使用參照點 (類似於方位點)。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 57d9ba37-819e-455f-9b22-bd7aabffe007
TQID: 'https://experienceleague.adobe.com/DXmhIshiUYoP-BlVe5cJFXbII9sEIdyo5YDkoKP-t0w'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 275
ht-degree: 28%

---

# FXG伺服器通訊協定{#fxg-server-protocol}

若要處理圖形，您可以使用參照點 (類似於方位點)。

使用參照點，您可以相對於某個特定參照點旋轉、縮放或調整圖形的大小。 參考點為`northWest`、`north`、`northEast`、`west`、`center`、`east`、`southWest`、`south`和`southeast`。 例如，使用中心參照點可將圖形中心旋轉45°。 下圖顯示參考點所在的位置、圖形、圖形從其`northWest`參考點旋轉20°，以及圖形從其`east`參考點旋轉20°。

![參考點影像](assets/wp_ref_points.png)

* A.參考點位置
* B. 圖形
* C.圖形從其`northWest`參考點旋轉20度
* D.圖形從其`east`參考點旋轉20度

語法如下：

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

預設值為none。 `inherit`值會將`s7:referencePoint`值（如果不是`none`）從頁面或群組層級的頂端傳給所有子項。 `none`設定表示物件沒有參考點，且使用FXG座標系。

>[!NOTE]
>
>若要使用參照點，並且該物件在處理之後不包含任何置換，請在處理該物件之後更新它的 x 和 y 值。

當來自`s7:referencePoint`的值用於群組（或路徑、線條元素或沒有明確寬度和高度定義的元素）時，該值會套用至群組的累積邊界方框。 例如，群組中所有物件之邊界方框的左上角做為群組的`northWest`參考點；右下角做為群組的`southEast`參考點。
