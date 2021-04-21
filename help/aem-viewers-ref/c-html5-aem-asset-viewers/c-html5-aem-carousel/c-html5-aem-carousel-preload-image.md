---
description: 預先載入影像是靜態資產預覽影像，直接在呼叫init()方法後載入，並在下載檢視器SDK程式庫、資產和預設集資訊時顯示。 預先載入影像的目的是視覺化地改善檢視器載入時間，並快速地向使用者呈現內容。
solution: Experience Manager
title: 預先載入影像
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,Business Practitioner
exl-id: 8caf156f-d641-44e9-94f9-5ba3245061a3
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---

# 預先載入影像{#preload-image}

預先載入影像是靜態資產預覽影像，直接在呼叫init()方法後載入，並在下載檢視器SDK程式庫、資產和預設集資訊時顯示。 預先載入影像的目的是視覺化地改善檢視器載入時間，並快速地向使用者呈現內容。

預先載入影像對於最常用的檢視器內嵌方法非常有效，即具有不受限高度的回應式內嵌。 請參閱標題[高度不受限制的自適應設計內嵌](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel.md#concept-b44f1df3c1c64d4e8b5565e7736bf95e)。

但是，當使用其他內嵌方法或特定設定選項時，此功能會有某些限制。 在下列情況下，預先載入影像可能無法正確呈現：

* 當檢視器大小固定且大小定義時，請在檢視器預設集記錄內使用`stagesize`組態屬性，或在頂層檢視器容器元素的外部檢視器CSS檔案中定義。
* 當使用具有寬度和高度定義的檢視器內嵌方法的彈性大小內嵌時。 請參閱標題[Flexible size embedding with width and height defined](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435)。

如果您在上述其中一個操作模式中使用檢視器，則可能需要使用`preloadImage`組態屬性來停用預先載入影像功能。

此外，即使在設定中啟用，也不會使用預先載入影像——如果檢視器內嵌在DOM元素中，則會使用`display:none` CSS設定來隱藏檢視器或從DOM樹狀結構中分離。
