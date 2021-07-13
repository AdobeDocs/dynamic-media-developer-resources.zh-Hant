---
description: 配置屬性直接定義為回應式影像程式庫所管理之IMG元素上的屬性。 每個影像都可以有其專屬的屬性集。
solution: Experience Manager
title: 命令參考 — 配置屬性
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8cc645f8-03fe-4ac7-b23f-36536b60fdf6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 1%

---

# 命令參考 — 配置屬性{#command-reference-configuration-attributes}

配置屬性直接定義為回應式影像程式庫所管理之IMG元素上的屬性。 每個影像都可以有其專屬的屬性集。

## data-src {#section-f52ff0f139604447a870abe6e1c03444}

選填。

影像伺服所提供影像的URL。 如果URL不存在，程式庫會使用在`src`屬性中設定的值作為後退。 此屬性提供初始影像和動態影像，由回應式影像庫從不同位置管理。

**範例**

```
<img data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## src {#section-5dbc1f9a3c274705adb9702e4c7af0b1}

若已設定`data-src`，則`src`為選用項目，且可包含您要新增的任何URL。 例如，它可以包含URL，指向程式庫所使用的相同影像伺服型影像。 或者，它可以包含GIF預留位置，甚至包含資料URI，以避免啟動時出現額外的伺服器往返。

如果未設定`data-src`，則`src`為必填項目，且必須包含影像伺服所提供影像的URL。

**範例**

使用`src`屬性的資料URI和`data-src`屬性的影像伺服URL:

```
<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## 資料斷點 {#section-3bf62a89ff3e40569848c1fe3ac7886c}

以逗號分隔的斷點清單，可選地後跟冒號(`:`)和影像伺服命令或影像預設集。 每個斷點是在邏輯CSS像素中定義的影像寬度值。 程式庫會從清單中載入具有最接近較大值的影像，並在用戶端上縮小影像，以符合執行階段CSS影像寬度。 （如果在高密度螢幕上工作，從伺服器載入的影像格式副本表示斷點值乘以設備的像素比）。

對於清單中的任何斷點，可以定義一個或多個影像伺服命令或影像預設集名稱。 此類額外參數僅應用於映像，以防此特定斷點當前處於活動狀態。

除了影響響應影像大小的視圖命令（如`wid=`、`hei=`或`scl=`）之外，您可以使用任何支援的「影像伺服」命令。 影像預設集也受到相同限制：與回應式影像庫搭配使用的影像預設集不得包含此類命令。

多個影像伺服命令或影像預設集名稱以「 `&`」字元分隔。 如果「影像伺服」命令的值中有逗號，則此類逗號將替換為`%2C`。 影像預設集名稱兩側加上貨幣符號(`$`)。

**範例**

**僅使用斷點**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720">`

**使用影像伺服命令**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:op_sharpen=1,720:resMode=sharp2&op_usm=0.9%2C1.0%2C8%2C0">`

**使用影像預設集**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:$ResponsiveImage_Low$,940:$ResponsiveImage_High$">`

**使用影像預設集和影像伺服命令**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:qlt=50,940:$ResponsiveImage_High$">`

## 資料模式 {#section-97caf43cf5ab4ca8b1b866d8f394a9a4}

AEM 6.4及更新版本以及Dynamic Media Viewers 5.9及更新版本提供下列兩種智慧型裁切模式：

* **手動**  — 在影像元素的屬性內定義用戶定義的斷點和相應的影像服務命令。
* **智慧型裁切**  — 計算的智慧型裁切轉譯會自動從傳送伺服器擷取。使用影像元素的運行時大小選擇最佳格式副本。

要使用智慧裁切模式，請將`data-mode`屬性設定為`smart crop`。

**範例**

```
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

當斷點更改時，關聯的映像元素在運行時分派`s7responsiveViewer`事件。

```
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
