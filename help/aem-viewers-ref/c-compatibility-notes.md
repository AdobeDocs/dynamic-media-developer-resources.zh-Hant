---
description: 作業系統、瀏覽器和行動裝置的相容性說明。
solution: Experience Manager
title: 相容性說明
feature: Dynamic Media Classic，檢視器，SDK/API
role: Developer,Business Practitioner
exl-id: 7ad499b1-7da6-483b-ab11-cff2eb9271da
source-git-commit: 62234233bb1a5bcbd0eac5d281b42ed785c0c169
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 1%

---

# 相容性說明{#compatibility-notes}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

作業系統、瀏覽器和行動裝置的相容性說明。

## BlackBerry® {#section-0c465ac3775d47fd838e2695a00abc45}

* 與舊版適用性視訊集不相容。 重新上傳可播放的最適化視訊集。

## 一般 {#section-7b9a9fcba85148d1802b7b3016b48e02}

* 當使用者放大至頁面時，瀏覽器端縮放會導致UI和影像變得模糊。 視縮放而定，使用者介面格式也會顯示不正確，並繼續呈現至全螢幕。
* 由於行動裝置上的大小限制，混合媒體檢視器使用投影片手勢來交換內嵌影像集中的幀，而非點選內嵌色票元件。 元件作為視覺指示器。
* 在Internet Explorer瀏覽器和某些觸控式裝置中，全螢幕模式不會佔據整個裝置畫面。 而是會將應用程式調整為瀏覽器視窗的大小。
* 關閉按鈕在iOS 8.0和iOS 8.1下無法運作，但在iOS 8.2下可運作。

## Galaxy SII {#section-dfd5f46f39834223b544b1e2f7a770c1}

* 使用縮放和eCatalog檢視器時出現記憶體洩漏。 透過框架重複導覽會導致瀏覽器當機。
* 在檢視器上點選兩下，會使整個頁面縮放，而非只啟用瀏覽器端縮放的檢視器。

## Galaxy S4 {#section-7effabfea75b488399e0f71cab4ce76b}

* 在瀏覽器設定中勾選全螢幕時，直向模式下的裝置偵測為平板電腦。

## Galaxy Nexus {#section-9340b0b026bd48e8a8a6b837b59c6dc5}

* 點選兩下檢視器會使整個頁面縮放，而非僅縮放檢視器，同時啟用瀏覽器端縮放。

## Galaxy Nexus 10和Galaxy平板電腦 {#section-ef52bd1249fe4f358c11838f7a557a00}

* eCatalog會以直向和橫向方向顯示錯誤的頁面跨頁。

## HTC行動裝置 {#section-dc42c80414c842e488738fc157c55b01}

* 無法停用原生代碼縮放是HTC UI包裝函式(HTC Sense)的「功能」。 在檢視器上使用「夾捏以縮放」手勢時，此功能會導致整個頁面縮放。 請改用雙鍵手勢。
* 如果影像地圖小且靠近，則影像地圖圖示會重疊。

## HTML5視訊檢視器 {#section-3c2dd1220dea4093b17ca2dd0a688307}

* `IntialBitRate` 修改器僅支援軟體HLS和FlashHDS播放。使用原生播放器時，無法運作。
* 不支援OGG和WebM漸進式播放。
* 瀏覽器縮放會導致視訊播放器以錯誤的大小顯示(包括Windows®控制面板顯示設定)。
* 在Safari上使用HLS串流的視訊搜尋不一致。

## Internet Explorer {#section-a18e8df396954f0b807017787c00aac7}

* 不支援怪異模式。
* 不支援相容模式。
* 不支援行動裝置上的Internet Explorer。

## iOS {#section-70161cba8c2044838d916d0b69c12247}

* 大型eCatalog導致iPad 2瀏覽器當機。

## Safari {#section-f8de598293d349188aa02c82cd3af8b6}

* Safari 6.1或更新版本：網際網路外掛程式設定會防止Flash視訊播放。
* 在Safari上使用HLS串流的視訊搜尋不一致。
* 無法在使用HLS串流的Safari 6上尋找視訊結尾。
