---
description: 作業系統、瀏覽器和行動裝置的相容性注意事項。
solution: Experience Manager
title: 相容性說明
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,Business Practitioner
exl-id: 7ad499b1-7da6-483b-ab11-cff2eb9271da
translation-type: tm+mt
source-git-commit: 62234233bb1a5bcbd0eac5d281b42ed785c0c169
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 1%

---

# 相容性說明{#compatibility-notes}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

作業系統、瀏覽器和行動裝置的相容性注意事項。

## BlackBerry® {#section-0c465ac3775d47fd838e2695a00abc45}

* 與舊版最適化視訊集不相容。 重新上傳最適化視訊集以允許播放。

## 一般 {#section-7b9a9fcba85148d1802b7b3016b48e02}

* 當使用者放大至頁面時，瀏覽器端縮放會導致UI和影像變得模糊。 使用者介面格式也會因縮放而不正確顯示，並傳至全螢幕。
* 由於行動裝置的大小限制，Mixed Media Viewer使用投影片手勢來交換內嵌影像集中的影格，而非點選內嵌色票元件。 元件作為可視指示器存在。
* 在Internet Explorer瀏覽器和某些觸控裝置中，全螢幕模式不會佔據整個裝置螢幕。 它會將應用程式調整為瀏覽器視窗的大小。
* 關閉按鈕在iOS 8.0和iOS 8.1下無法運作，但在iOS 8.2下可運作。

## Galaxy SIII {#section-dfd5f46f39834223b544b1e2f7a770c1}

* 使用縮放和eCatalog檢視器時，會出現記憶體洩漏。 在影格中重複導覽會導致瀏覽器當機。
* 點選兩下檢視器會使整個頁面縮放，而不是只讓檢視器啟用瀏覽器端縮放。

## Galaxy S4 {#section-7effabfea75b488399e0f71cab4ce76b}

* 在縱向模式中偵測為平板電腦的裝置，並在瀏覽器設定中勾選「全螢幕」。

## Galaxy Nexus {#section-9340b0b026bd48e8a8a6b837b59c6dc5}

* 點選兩下檢視器可讓整個頁面縮放，而非只縮放檢視器，並啟用瀏覽器端縮放。

## Galaxy Nexus 10和Galaxy Tablet {#section-ef52bd1249fe4f358c11838f7a557a00}

* eCatalog會以縱向和橫向方向顯示不正確的頁面跨頁。

## HTC行動裝置{#section-dc42c80414c842e488738fc157c55b01}

* 無法停用原生夾捏縮放是HTC UI包裝函式(HTC Sense)的「功能」。 在檢視器上使用「夾捏以縮放」手勢時，此功能可導致整個頁面縮放。 請改用點選兩下手勢。
* 如果影像地圖較小且靠近，影像地圖圖示會重疊。

## HTML5 Video Viewer {#section-3c2dd1220dea4093b17ca2dd0a688307}

* `IntialBitRate` 僅軟體HLS和FlashHDS回放支援修改器。當播放使用原生播放器時，它無法運作。
* 不支援OGG和WebM漸進式播放。
* 瀏覽器縮放會使視訊播放器以不正確的大小顯示（包括Windows®控制面板顯示設定）。
* 在Safari上使用HLS串流的視訊搜尋不一致。

## Internet Explorer {#section-a18e8df396954f0b807017787c00aac7}

* 不支援Quirks模式。
* 不支援相容模式。
* 不支援行動裝置上的Internet Explorer。

## iOS {#section-70161cba8c2044838d916d0b69c12247}

* 大型的eCatalog會導致瀏覽器在iPad 2上當機。

## Safari {#section-f8de598293d349188aa02c82cd3af8b6}

* Safari 6.1或更新版本：網際網路外掛程式設定無法播放Flash視訊。
* 在Safari上使用HLS串流的視訊搜尋不一致。
* 無法在使用HLS串流的Safari 6上尋找視訊結束。
