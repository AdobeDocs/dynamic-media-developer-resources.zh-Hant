---
title: 相容性說明
description: 作業系統、瀏覽器和移動設備的相容性說明。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 7ad499b1-7da6-483b-ab11-cff2eb9271da
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 1%

---

# 相容性說明{#compatibility-notes}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

作業系統、瀏覽器和移動設備的相容性說明。

## BlackBerry® {#section-0c465ac3775d47fd838e2695a00abc45}

* 與較舊的自適應視頻集不相容。 重新上載自適應視頻集以允許播放。

## 一般 {#section-7b9a9fcba85148d1802b7b3016b48e02}

* 瀏覽器端縮放會導致用戶將UI和影像縮放到頁面時變得模糊。 用戶介面格式設定也會根據縮放情況顯示不正確，並會轉到全屏。
* 由於移動設備的大小限制，混合媒體查看器使用幻燈片手勢來交換嵌入影像集中的幀，而不是點擊嵌入的色板元件。 元件作為視覺指示器存在。
* 在Internet Explorer瀏覽器和某些觸摸設備中，全屏模式不佔用整個設備螢幕。 相反，它會根據瀏覽器窗口的大小調整應用程式的大小。
* 「關閉」按鈕在iOS8.0和iOS8.1下不起作用，但在iOS8.2下起作用。

## 銀河SII {#section-dfd5f46f39834223b544b1e2f7a770c1}

* 在「縮放」和「電子目錄」查看器中出現記憶體洩漏。 通過框架重複導航會導致瀏覽器崩潰。
* 在查看器上按兩下可使整個頁面縮放，而不是僅使用啟用了瀏覽器側縮放的查看器。

## 銀河S4 {#section-7effabfea75b488399e0f71cab4ce76b}

* 在瀏覽器設定中選中「Full Screen（全屏）」後，在縱向模式下檢測到設備為平板電腦。

## 銀河系 {#section-9340b0b026bd48e8a8a6b837b59c6dc5}

* 在查看器上按兩下可使整個頁面縮放，而不是僅縮放查看器，同時啟用瀏覽器側縮放。

## Galaxy Nexus 10和Galaxy平板電腦 {#section-ef52bd1249fe4f358c11838f7a557a00}

* eCatalog顯示具有縱向和橫向方向的頁面跨頁不正確。

## HTC移動設備 {#section-dc42c80414c842e488738fc157c55b01}

* 無法禁用本機收縮縮放是HTC UI包裝(HTC Sense)的「功能」。 在查看器上使用「收縮縮放」手勢時，此功能可導致整個頁面縮放。 請改用按兩下手勢。
* 如果影像映射較小且靠近在一起，則影像映射表徵圖會重疊。

## HTML5視頻查看器 {#section-3c2dd1220dea4093b17ca2dd0a688307}

* `IntialBitRate` 只有軟體HLS和FlashHDS回放才支援修改量。 當播放使用本機播放器時，它不工作。
* 不支援OGG和WebM漸進式回放。
* 瀏覽器縮放導致視頻播放器顯示大小不正確（包括Windows®控制面板顯示設定）。
* 使用Safari上的HLS流的視頻查找不一致。

## Internet Explorer {#section-a18e8df396954f0b807017787c00aac7}

* 不支援Quirks模式。
* 不支援相容模式。
* 不支援移動上的Internet Explorer。

## iOS {#section-70161cba8c2044838d916d0b69c12247}

* 大型eCatalog導致瀏覽器在iPad2上崩潰。

## Safari {#section-f8de598293d349188aa02c82cd3af8b6}

* Safari 6.1或更高版本：Internet插件設定阻止Flash視頻播放。
* 使用Safari上的HLS流的視頻查找不一致。
* 無法使用HLS流在Safari 6上查找視頻結束。
