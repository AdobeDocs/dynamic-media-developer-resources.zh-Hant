---
title: 預載入影像
description: 預載入影像是靜態資產預覽影像，它在調用init()方法後立即載入，並在下載Viewer SDK庫、資產和預設資訊時顯示。 該預載影像的目的是直觀地改善觀看者的載入時間，並快速地向用戶呈現內容。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 8caf156f-d641-44e9-94f9-5ba3245061a3
source-git-commit: 4aaa77b1fb58b30b02ee15f6080169fa354d5907
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# 預載入影像{#preload-image}

預載入影像是靜態資產預覽影像，它在調用init()方法後立即載入，並在下載Viewer SDK庫、資產和預設資訊時顯示。 該預載影像的目的是直觀地改善觀看者的載入時間，並快速地向用戶呈現內容。

預載入影像對於最常見的查看器嵌入方法效果很好，該方法具有響應性，且高度不受限制。 查看標題 [具有無限制高度的響應設計嵌入](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel.md#concept-b44f1df3c1c64d4e8b5565e7736bf95e)。

但是，當使用其他嵌入方法或特定配置選項時，該功能具有某些限制。 在以下情況下，預載入影像可能無法正確呈現：

* 當查看器的大小固定且大小定義為 `stagesize` 在查看器預設記錄或頂級查看器容器元素的外部查看器CSS檔案中的configuration屬性。
* 當使用具有寬度和高度定義的查看器嵌入方法的柔性尺寸嵌入時。 查看標題 [定義寬度和高度的柔性尺寸嵌入](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435)。

如果在上面列出的操作模式之一中使用查看器，請使用 `preloadImage` 配置屬性。

此外，即使在配置中啟用，也不會使用預載入影像 — 如果查看器嵌入到DOM元素中，則使用 `display:none` CSS設定或從DOM樹分離。
