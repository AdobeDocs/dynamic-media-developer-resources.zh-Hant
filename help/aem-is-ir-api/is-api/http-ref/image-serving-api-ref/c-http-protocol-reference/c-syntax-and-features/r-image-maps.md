---
description: IS提供簡化HTML影像地圖使用的機制。 IS中以JAVA為基礎和以Flash為基礎的檢視器也包含對影像地圖的有限支援。
solution: Experience Manager
title: 影像地圖
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---


# 影像地圖{#image-maps}

IS提供簡化HTML影像地圖使用的機制。 IS中以JAVA為基礎和以Flash為基礎的檢視器也包含對影像地圖的有限支援。

源影像映射通過`catalog::Map`或通過`map=`命令提供給IS，並且使用`req=map`命令檢索處理過的映射。

影像地圖由一或多個HTML AREA元素組成，並以&#39;&lt;&#39;和&#39;>&#39;正確分隔。 如果透過目錄：:Map提供，則所有像素座標值都假設為原始影像解析度，且相對於（未修改）來源影像的左上角。 通過`map=`命令提供時，坐標值假定為相對於層左上角（`rotate=`和`extend=`之後）的層坐標。

>[!NOTE]
>
>目前不允許%座標，而且可能會處理錯誤。

IS通過將空間變換（例如縮放和旋轉）應用於映射坐標，然後以適當的z順序（前後）和適當的定位來從每個組成層的源影像映射生成複合影像映射。

當與`req=map`（直接在請求中、透過目錄範本或`catalog::Modifier`字串中）一起提供時，會考慮使用下列命令來處理影像地圖：

* `align=`
* `wid=`
* `hei=`
* `scl=`
* `crop=`
* `flip=`
* `rotate=`
* `scale=`
* `layer=`
* `size=`
* `extend=`
* `origin=`
* `pos=`
* `anchor=`
* `src=`
* `map=`

其他所有命令都被有效忽略。

在處理`req=map`請求期間可修改`SHAPE`和`COORDS`屬性，不修改`AREA`元素的所有其它屬性都被傳遞。 `AREA`在大多數情況下，這包括將`SHAPE`值從`DEFAULT`變更為`RECT`（這也會新增`COORDS`屬性），或變更`COORDS`值。

任何在處理期間變成空白的`AREA`元素都會完全移除。 如果映射與`layer=comp`關聯，則它會放在所有其他映射後面。 資料會以文字形式一傳回，成為或多個HTML `AREA`元素。 空回覆字串表示指定物件沒有影像對應。

圖層透明度不會被視為地圖處理。 完全透明的圖層仍然可以具有與其相關聯的影像映射。 部分透明層的映射不會被修剪到透明區域。

## 另請參閱 {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) , [catalog::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [HTML 4.01規格](http://www.w3.org/TR/html401/)
