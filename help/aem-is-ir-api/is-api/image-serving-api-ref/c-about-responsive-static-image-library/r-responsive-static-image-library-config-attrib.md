---
description: 配置屬性直接定義為「自適應影像庫」管理的IMG元素上的屬性。 每個影像都可以有其專屬的屬性集。
solution: Experience Manager
title: 命令參考——配置屬性
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---


# 命令參考——配置屬性{#command-reference-configuration-attributes}

配置屬性直接定義為「自適應影像庫」管理的IMG元素上的屬性。 每個影像都可以有其專屬的屬性集。

## data-src {#section-f52ff0f139604447a870abe6e1c03444}

選填。

影像伺服所提供影像的URL。 如果URL不存在，程式庫會使用在`src`屬性中設定的值做為回落。 此屬性可支援互動式影像庫從不同位置管理的初始影像和動態影像。

**範例**

```
<img data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## src {#section-5dbc1f9a3c274705adb9702e4c7af0b1}

如果設定`data-src`，則`src`為選用項目，且可包含您要新增的任何URL。 例如，它可包含資料庫所使用之相同影像伺服影像的URL。 或者，它可包含GIF預留位置，或甚至資料URI，以避免啟動時出現額外的伺服器往返。

如果未設定`data-src`，則`src`為必填項目，且必須包含影像伺服所用影像的URL。

**範例**

使用`src`屬性的資料URI和`data-src`屬性的影像伺服URL:

```
<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## data-breakpoints {#section-3bf62a89ff3e40569848c1fe3ac7886c}

以逗號分隔的中斷點清單，並可選地後面加上冒號(`:`)和影像伺服命令或影像預設集。 每個斷點都是以邏輯CSS像素定義的影像寬度值。 程式庫會從清單中載入最大值的影像，並在用戶端上縮放影像，以符合執行時期的CSS影像寬度。 （如果您在高密度螢幕上工作，從伺服器載入的影像轉譯代表斷點值乘以裝置的像素比例）。

對於清單中的任何斷點，可以定義一個或多個影像服務命令或影像預設集名稱。 這些額外參數只會套用至影像，以防此特定的斷點目前處於作用中。

除了那些影響響應影像大小的視圖命令（如`wid=`、`hei=`或`scl=`）外，您可以使用任何受支援的「影像服務」命令。 影像預設集的限制也相同：與自適應影像庫一起使用的影像預設集不得包含此類命令。

多個影像伺服命令或影像預設集名稱會以&quot; `&`&quot;字元分隔。 如果「影像伺服」命令的值中有逗號，則會以`%2C`取代此類逗號。 「影像預設集」名稱會以貨幣符號(`$`)包住。

**範例**

**僅使用中斷點**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720">`

**使用影像伺服命令**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:op_sharpen=1,720:resMode=sharp2&op_usm=0.9%2C1.0%2C8%2C0">`

**使用影像預設集**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:$ResponsiveImage_Low$,940:$ResponsiveImage_High$">`

**使用影像預設集和影像伺服命令**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:qlt=50,940:$ResponsiveImage_High$">`

## data-mode {#section-97caf43cf5ab4ca8b1b866d8f394a9a4}

以下兩種智慧型裁切模式適用於AEM6.4和更新版本，以及Dynamic Media檢視器5.9和更新版本：

* **手動** -用戶定義的斷點和相應的「影像服務」命令在影像元素的屬性中定義。
* **智慧型裁切** -計算的智慧型裁切轉譯會自動從傳送伺服器擷取。使用影像元素的執行時期大小來選取最佳轉譯。

要使用智慧裁切模式，請將`data-mode`屬性設定為`smart crop`。

**範例**

```
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

當斷點變更時，關聯的映像元素在運行時間中調度`s7responsiveViewer`事件。

```
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```

