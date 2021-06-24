---
description: IS提供簡化HTML影像地圖使用的機制。 IS中以JAVA為基礎和以Flash為基礎的檢視器，也包含對影像地圖的有限支援。
solution: Experience Manager
title: 影像地圖
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 9a685f9d-205d-43b3-b5fe-3ae324fe153e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# 影像地圖{#image-maps}

IS提供簡化HTML影像地圖使用的機制。 IS中以JAVA為基礎和以Flash為基礎的檢視器，也包含對影像地圖的有限支援。

通過`catalog::Map`或使用`map=`命令向IS提供源影像映射，並使用`req=map`命令檢索處理的映射。

影像地圖由一或多個HTML AREA元素組成，並以「&lt;」和「>」正確分隔。 如果是透過catalog::Map提供，則所有像素坐標值都假設為原始影像解析度，且相對於（未修改的）源影像的左上角。 通過`map=`命令提供時，坐標值被假定為相對於層的左上角（在`rotate=`和`extend=`之後）的層坐標。

>[!NOTE]
>
>目前不允許%座標，處理可能會不正確。

IS通過將空間變換（例如縮放和旋轉）應用到地圖坐標，然後以適當的z階（前後）和適當的定位來裝配處理的圖層映射，從每個組成層的源影像映射中生成複合影像映射。

當與`req=map`一起提供時（直接在請求中、透過目錄範本，或在`catalog::Modifier`字串中），會考量下列命令進行影像對應處理：

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

其他所有命令都會被有效忽略。

在處理`req=map`請求期間，可修改`SHAPE`和`COORDS`屬性，而未修改地傳遞`AREA`元素的所有其它屬性。 `AREA`在大多數情況下，這包括將`SHAPE`值從`DEFAULT`變更為`RECT`（這也會新增`COORDS`屬性），或變更`COORDS`值。

任何在處理期間變為空的`AREA`元素將會完全移除。 如果映射與`layer=comp`關聯，則它被放在所有其他映射後面。 資料以文本形式返回，格式為一個或多個HTML `AREA`元素。 空回覆字串表示指定物件沒有影像對應。

地圖處理時不會考慮圖層透明度。 完全透明的圖層仍然可以有與其相關聯的影像映射。 部分透明層的映射不會被修剪到透明區域。

## 另請參閱 {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) ,  [catalog::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md),  [HTML 4.01規格](http://www.w3.org/TR/html401/)
