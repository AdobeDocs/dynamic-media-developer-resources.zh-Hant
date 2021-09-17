---
title: 預載影像
description: 預先載入影像是靜態資產預覽影像，在呼叫init()方法後立即載入，並在下載檢視器SDK程式庫、資產和預設集資訊時顯示。 該預載入影像的目的是以視覺化方式改善檢視器載入時間，並快速地向使用者呈現內容。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 8caf156f-d641-44e9-94f9-5ba3245061a3
source-git-commit: 4aaa77b1fb58b30b02ee15f6080169fa354d5907
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# 預載影像{#preload-image}

預先載入影像是靜態資產預覽影像，在呼叫init()方法後立即載入，並在下載檢視器SDK程式庫、資產和預設集資訊時顯示。 該預載入影像的目的是以視覺化方式改善檢視器載入時間，並快速地向使用者呈現內容。

預載入影像對於最常見的查看器嵌入方法是有效的，即具有不受限高度的響應嵌入。 請參閱標題[高度不受限制的回應式設計內嵌](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel.md#concept-b44f1df3c1c64d4e8b5565e7736bf95e)。

但是，使用其他內嵌方法或特定設定選項時，此功能會有某些限制。 在下列情況下，預載影像可能無法正確呈現：

* 當檢視器大小固定且大小已定義時，請在檢視器預設集記錄內使用`stagesize`組態屬性，或在頂層檢視器容器元素的外部檢視器CSS檔案中使用。
* 使用具有檢視器內嵌寬度和高度定義方法的彈性大小內嵌時。 請參閱標題[定義了寬度和高度的靈活大小嵌入](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435)。

如果在上面列出的操作模式之一中使用查看器，請使用`preloadImage`配置屬性禁用預載入影像功能。

此外，即使在設定中啟用，也不會使用預先載入影像 — 如果檢視器內嵌至DOM元素，則會使用`display:none` CSS設定來隱藏，或從DOM樹狀結構中分離。
