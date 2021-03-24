---
description: 預先載入影像是靜態資產預覽影像，直接在呼叫init()方法後載入，並在下載檢視器SDK程式庫、資產和預設集資訊時顯示。 預先載入影像的目的是視覺化地改善檢視器載入時間，並快速地向使用者呈現內容。
solution: Experience Manager
title: 預先載入影像
feature: Dynamic Media經典，檢視器，SDK/API，互動式影像
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---


# 預先載入影像{#preload-image}

預先載入影像是靜態資產預覽影像，直接在呼叫init()方法後載入，並在下載檢視器SDK程式庫、資產和預設集資訊時顯示。 預先載入影像的目的是視覺化地改善檢視器載入時間，並快速地向使用者呈現內容。

預先載入影像對於最常用的檢視器內嵌方法非常有效，即具有不受限高度的回應式內嵌。 請參閱標題[高度不受限制的自適應設計內嵌](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435)。

但是，當使用其他內嵌方法或特定設定選項時，此功能會有某些限制。 在下列情況下，預先載入影像可能無法正確呈現：

* 當檢視器大小固定且大小定義時，請在檢視器預設集記錄內使用`stagesize`組態屬性，或在頂層檢視器容器元素的外部檢視器CSS檔案中定義。
* 當使用具有寬度和高度定義的檢視器內嵌方法的彈性大小內嵌時。 請參閱標題[Flexible size embedding with width and height defined](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435)。

如果您在上述其中一個操作模式中使用檢視器，則可能需要使用`preloadImage`組態屬性來停用預先載入影像功能。

此外，即使在設定中啟用，也不會使用預先載入影像——如果檢視器內嵌在DOM元素中，則會使用`display:none` CSS設定來隱藏檢視器或從DOM樹狀結構中分離。
