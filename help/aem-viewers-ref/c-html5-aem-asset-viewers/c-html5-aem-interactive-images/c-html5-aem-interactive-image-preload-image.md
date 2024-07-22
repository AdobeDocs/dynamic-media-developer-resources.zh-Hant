---
title: 預先載入影像
description: 預先載入影像是靜態資產預覽影像，在呼叫init()方法後立即載入，並在下載檢視器SDK程式庫、資產和預設集資訊時顯示。 預先載入影像的目的是在視覺上改善檢視器載入時間，並快速向使用者呈現內容。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 54bea5fc-916c-4a58-bc06-b726884d488a
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# 預先載入影像{#preload-image}

預先載入影像是靜態資產預覽影像，在呼叫init()方法後立即載入，並在下載檢視器SDK程式庫、資產和預設集資訊時顯示。 預先載入影像的目的是在視覺上改善檢視器載入時間，並快速向使用者呈現內容。

預先載入影像適用於最常見的檢視器內嵌方法，也就是以不受限制的高度回應式內嵌。 檢視標題[高度不受限制的回應式設計內嵌](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435)。

不過，此功能在使用其他內嵌方法或特定組態選項時有一定的限制。 在下列情況下，預先載入影像可能無法正確轉譯：

* 當檢視器的大小已固定，且大小是使用檢視器預設集記錄中的`stagesize`組態屬性來定義時。 或者，使用頂層檢視器容器元素的外部檢視器CSS檔案。
* 使用彈性大小內嵌，搭配定義寬度與高度的檢視器內嵌方法時。 檢視標題[定義寬度和高度的彈性大小內嵌](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435)。

如果您在上面列出的其中一個作業模式中使用檢視器，請停用使用`preloadImage`設定屬性的預先載入影像功能。

此外，即使已在設定中啟用，也不會使用預先載入影像，前提是使用`display:none` CSS設定隱藏檢視器內嵌至DOM元素，或是從DOM樹狀結構中斷連線。
