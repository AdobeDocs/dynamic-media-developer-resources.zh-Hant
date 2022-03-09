---
description: 配置屬性直接定義為響應影像庫管理的IMG元素上的屬性。 每個影像可以有其自己的屬性集。
solution: Experience Manager
title: 命令引用 — 配置屬性
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8cc645f8-03fe-4ac7-b23f-36536b60fdf6
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 1%

---

# 命令引用 — 配置屬性{#command-reference-configuration-attributes}

配置屬性直接定義為響應影像庫管理的IMG元素上的屬性。 每個影像可以有其自己的屬性集。

## 資料源 {#section-f52ff0f139604447a870abe6e1c03444}

選填。

影像服務所用影像的URL。 如果URL不存在，庫將使用中設定的值 `src` 屬性。 此屬性用於響應映像庫從不同位置管理的初始映像和動態映像。

**範例**

```
<img data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## 高 {#section-5dbc1f9a3c274705adb9702e4c7af0b1}

如果 `data-src` 已設定， `src` 是可選的，並且可以包含要添加的任何URL。 例如，它可以包含庫使用的同一基於影像服務的影像的URL。 或者，它可以包含GIF佔位符，甚至包含資料URI，以避免在啟動時出現額外的伺服器往返。

如果 `data-src` 沒有設定， `src` 必需，並且必須包含Image Serving所用映像的URL。

**範例**

使用資料URI `src` 屬性和影像服務URL `data-src` 屬性：

```
<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## 資料斷點 {#section-3bf62a89ff3e40569848c1fe3ac7886c}

以逗號分隔的斷點清單，可選後跟冒號( `:`)和「影像服務」命令或「影像預設」。 每個斷點是在邏輯CSS像素中定義的影像寬度值。 庫從清單中載入具有最大值的影像，並在客戶端上縮放影像，以匹配運行時CSS影像寬度。 （如果在高密度螢幕上工作，從伺服器載入的影像呈現形式表示斷點值乘以設備的像素比率）。

對於清單中的任何斷點，可以定義一個或多個影像服務命令或影像預設名稱。 此類額外參數僅應用於影像，以防此特定斷點當前處於活動狀態。

除了那些影響響應影像大小的視圖命令外，您可以使用任何受支援的「影像服務」命令，如 `wid=`。 `hei=`或 `scl=`。 同樣的限制適用於「影像預設」：與響應影像庫一起使用的影像預設不得包含此類命令。

多個影像服務命令或影像預設名稱與「」分隔 `&`&quot;字元。 如果「影像服務」命令的值中包含逗號，則此逗號將替換為 `%2C`。 影像預設名稱用美元符號( `$`)。

**範例**

**僅使用斷點**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720">`

**使用影像服務命令**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:op_sharpen=1,720:resMode=sharp2&op_usm=0.9%2C1.0%2C8%2C0">`

**使用影像預設**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:$ResponsiveImage_Low$,940:$ResponsiveImage_High$">`

**使用影像預設和影像服務命令**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:qlt=50,940:$ResponsiveImage_High$">`

## 資料模式 {#section-97caf43cf5ab4ca8b1b866d8f394a9a4}

以下兩種智慧裁剪模式在AEM6.4及更高版本和Dynamic Media觀眾5.9及更高版本中提供：

* **手動**  — 用戶定義的斷點和相應的映像服務命令在映像元素的屬性中定義。
* **智慧裁剪**  — 計算的智慧裁剪格式副本自動從交付伺服器中檢索。 使用影像元素的運行時大小選擇最佳格式副本。

要使用智慧裁剪模式，請設定 `data-mode` 屬性 `smart crop`。

**範例**

```html {.line-numbers}
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

相關影像元素分配 `s7responsiveViewer` 斷點更改時的運行時事件。

```html {.line-numbers}
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
