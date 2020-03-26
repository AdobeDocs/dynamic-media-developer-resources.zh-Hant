---
description: IS提供簡化HTML影像地圖使用的機制。 IS中以JAVA為基礎和以Flash為基礎的檢視器也包含對影像地圖的有限支援。
seo-description: IS提供簡化HTML影像地圖使用的機制。 IS中以JAVA為基礎和以Flash為基礎的檢視器也包含對影像地圖的有限支援。
seo-title: 影像地圖
solution: Experience Manager
title: 影像地圖
topic: Scene7 Image Serving - Image Rendering API
uuid: 2b7b620b-712b-4110-ba38-993a354c09d3
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# Image maps{#image-maps}

IS提供簡化HTML影像地圖使用的機制。 IS中以JAVA為基礎和以Flash為基礎的檢視器也包含對影像地圖的有限支援。

源影像映射通過命令提供給IS, `catalog::Map` 或用該命 `map=` 令提供給IS，並且使用該命令檢索處理過的映 `req=map` 射。

影像地圖由一或多個HTML AREA元素組成，並以&#39;&lt;&#39;和&#39;>&#39;正確分隔。 如果透過目錄：:Map提供，則所有像素座標值都假設為原始影像解析度，且相對於（未修改）來源影像的左上角。 通過命令提 `map=` 供時，坐標值假定為相對於圖層左上角（在和之後）的圖層 `rotate=` 坐 `extend=`標。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>目前不允許%座標，而且可能會處理錯誤。

IS通過將空間變換（例如縮放和旋轉）應用於映射坐標，然後以適當的z順序（前後）和適當的定位來從每個組成層的源影像映射生成複合影像映射。

當與（直接在請求中、透過目錄範本或字串中）一起提供時， `req=map` 會將下列指令視為影像地圖處理 `catalog::Modifier` 用途：

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

在處 `SHAPE` 理請求期間，可以修 `COORDS` 改元素的屬性和屬性，不進行修改 `AREA``req=map``AREA` 而傳遞元素的所有其他屬性。 在大多數情況下，這包 `SHAPE` 括將值 `DEFAULT` 從 `RECT` 更改為(這也會添加屬 `COORDS` 性)或更改 `COORDS` 值。

任何 `AREA` 在處理期間變成空白的元素都會完全移除。 如果地圖與之關聯， `layer=comp` 則會置於所有其他地圖後面。 資料會以文字形式一傳回，成為或多個HTML `AREA` 元素。 空回覆字串表示指定物件沒有影像對應。

圖層透明度不會被視為地圖處理。 完全透明的圖層仍然可以具有與其相關聯的影像映射。 部分透明層的映射不會被修剪到透明區域。

## 另請參閱 {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) , [catalog::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [HTML 4.01規格](http://www.w3.org/TR/html401/)
