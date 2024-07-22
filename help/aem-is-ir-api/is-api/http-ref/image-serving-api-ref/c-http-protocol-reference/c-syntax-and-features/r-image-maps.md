---
description: IS提供簡化HTML影像地圖使用的機制。 IS中的JAVA型和Flash型檢視器也包含對影像地圖的有限支援。
solution: Experience Manager
title: 影像地圖
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9a685f9d-205d-43b3-b5fe-3ae324fe153e
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---

# 影像地圖{#image-maps}

IS提供簡化HTML影像地圖使用的機制。 IS中的JAVA型和Flash型檢視器也包含對影像地圖的有限支援。

透過`catalog::Map`或使用`map=`命令將Source影像地圖提供給IS，並使用`req=map`命令擷取已處理的地圖。

影像地圖由一或多個HTMLAREA元素組成，並以&#39;&lt;&#39;和&#39;>&#39;正確分隔。 如果透過catalog：：Map提供，則所有畫素座標值都會假設為使用原始影像解析度，並且相對於（未修改的）來源影像左上角。 透過`map=`命令提供時，座標值會假設為圖層座標，相對於圖層的左上角（`rotate=`與`extend=`之後）。

>[!NOTE]
>
>目前不允許使用%座標，且處理方式可能不正確。

IS會透過將空間轉換（例如縮放和旋轉）套用至地圖座標，然後以適當的z順序（從前到後）組裝處理過的圖層地圖，從每個組成圖層的來源影像地圖產生複合影像地圖。

與`req=map`一起提供時（直接在要求中、透過目錄範本或在`catalog::Modifier`字串中），會考慮使用下列命令來處理影像地圖：

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

所有其他指令都會被有效忽略。

處理`req=map`要求期間，`AREA`的`SHAPE`和`COORDS`屬性可能會修改，`AREA`專案的所有其他屬性都會不經修改而傳遞。 在大多數情況下，這涉及將`SHAPE`值從`DEFAULT`變更為`RECT` （這也會新增`COORDS`屬性），或變更`COORDS`值。

處理期間變為空白的任何`AREA`元素都會完全移除。 如果地圖與`layer=comp`相關聯，則會將其置於所有其他地圖之後。 資料以文字形式傳回，作為一或多個HTML`AREA`元素。 空白的回覆字串表示指定的物件沒有影像地圖。

處理地圖時不會考量圖層透明度。 完全透明的圖層仍然可以有與其關聯的影像地圖。 部分透明圖層的對映不會裁剪至透明區域。

## 另請參閱 {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) ， [目錄：：Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md)， [HTML4.01規格](https://www.w3.org/TR/html401/)
