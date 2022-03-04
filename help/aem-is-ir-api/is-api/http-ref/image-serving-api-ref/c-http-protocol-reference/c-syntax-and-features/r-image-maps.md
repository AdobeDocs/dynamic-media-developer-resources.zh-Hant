---
description: IS提供了簡化HTML影像映射使用的機制。 IS中基於JAVA和基於Flash的查看器也包括對影像映射的有限支援。
solution: Experience Manager
title: 影像映射
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9a685f9d-205d-43b3-b5fe-3ae324fe153e
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%

---

# 影像映射{#image-maps}

IS提供了簡化HTML影像映射使用的機制。 IS中基於JAVA和基於Flash的查看器也包括對影像映射的有限支援。

源影像映射通過 `catalog::Map` 或 `map=` 命令，並使用 `req=map` 的子菜單。

影像映射由一個或多個HTMLAREA元素組成，正確地用「&lt;」和「>」分隔。 如果通過catalog::Map提供，則所有像素坐標值都假定為原始影像解析度，並且相對於（未修改的）源影像的左上角。 當通過 `map=` 命令，坐標值假定為相對於圖層左上角的圖層坐標(在 `rotate=` 和 `extend=`)。

>[!NOTE]
>
>此時不允許%坐標，可能處理不正確。

IS通過將空間變換（如縮放和旋轉）應用到地圖坐標，然後按適當的z階（前後）和適當的定位組合處理的圖層地圖，從每個組成層的源影像地圖生成複合影像地圖。

當與 `req=map` (直接在請求中、通過目錄模板或在 `catalog::Modifier` 字串):

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

的 `SHAPE` 和 `COORDS` 屬性 `AREA` 在處理 `req=map` 請求，所有其他屬性 `AREA` 元素將在不修改的情況下傳遞。 在大多數情況下，這涉及更改 `SHAPE` 值 `DEFAULT` 至 `RECT` (這也會增加 `COORDS` 屬性)，或更改 `COORDS` 值。

任意 `AREA` 在處理過程中變為空的元素將被完全刪除。 如果映射與 `layer=comp` 它被放在所有其他地圖後面。 以文本形式返回資料作為或多個HTML `AREA` 元素。 空答復字串表示指定對象不存在影像映射。

圖處理不考慮層透明度。 完全透明的層仍然可以具有與其相關聯的影像映射。 部分透明層的映射不會被剪切到透明區域。

## 另請參閱 {#see-also}

[地圖=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) 。 [目錄：：映射](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md)。 [HTML4.01規格](https://www.w3.org/TR/html401/)
