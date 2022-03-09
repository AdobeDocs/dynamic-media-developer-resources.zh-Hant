---
title: 彈出
description: Flyout Viewer是影像查看器。 它顯示靜態影像，其縮放版本顯示在用戶激活的彈出視圖中。 此查看器可與影像集配合使用，並使用色板完成導航。 它設計用於台式機和移動設備。
keywords: 響應
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 9b60330f-5348-431d-9682-cf97aace3679
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2065'
ht-degree: 0%

---

# 彈出{#flyout}

Flyout Viewer是影像查看器。 它顯示靜態影像，其縮放版本顯示在用戶激活的彈出視圖中。 此查看器可與影像集配合使用，並使用色板完成導航。 它設計用於台式機和移動設備。

>[!NOTE]
>
>此查看器不支援使用IR（影像呈現）或UGC（用戶生成的內容）的影像。

查看器類型為504。

請參閱 [系統要求和先決條件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

## 演示URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## 使用浮出查看器 {#section-f21ac23d3f6449ad9765588d69584772}

Flyout Viewer表示主JavaScript檔案和一組幫助檔案(單個JavaScript包含該查看器在運行時下載的所有Viewer SDK元件，由該查看器使用

Flyout Viewer僅用於嵌入式，這意味著它使用文檔化的API整合到網頁中。 Flyout Viewer沒有可用於生產的網頁。

配置和外觀與其他查看器類似。 可以使用自定義CSS應用外觀。

請參閱 [所有查看器通用的命令引用 — 配置屬性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 和 [所有查看器通用的命令引用 — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 與Flyout查看器交互 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Flyout Viewer支援其他移動應用程式中常見的單點觸控和多點觸控手勢。

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>手勢 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>按一下 </p> </td> 
   <td colname="col2"> <p> 激活彈出視圖或主縮放級別和次縮放級別之間的更改。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>水準輕掃或輕拂 </p> </td> 
   <td colname="col2"> <p> 在色板欄中滾動色板清單。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直滑動 </p> </td> 
   <td colname="col2"> <p>如果手勢是在色板區域內完成的，則它將執行本機頁面滾動。 </p> </td> 
  </tr> 
 </tbody> 
</table>

該查看器還支援Windows設備上的觸摸輸入和滑鼠輸入，包括觸摸屏和滑鼠。 但是，此支援僅限於Chrome、Internet Explorer 11和Edge Web瀏覽器。

此查看器可完全以鍵盤方式訪問。

請參閱 [鍵盤輔助功能和導航](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 嵌入浮出查看器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同的網頁對查看者行為有不同的需求。 該網頁可具有靜態頁面佈局，或使用在不同設備上顯示不同的響應設計，或對不同瀏覽器窗口大小的響應設計。 為滿足這些需要，查看器支援兩種主要操作模式：固定尺寸嵌入和響應性設計嵌入。

當查看器在初始載入後不更改其大小時，使用固定大小嵌入模式。 此選項最適合具有靜態頁面佈局的網頁。

響應性設計嵌入模式假定查看器必須在運行時調整大小以響應其容器的大小變化 `DIV`。 最常見的用例是向使用靈活頁面佈局的網頁添加查看器。

將響應性設計嵌入模式與浮動查看器一起使用時，請確保使用 `imagereload` 的下界。 理想情況下，按照網頁CSS的要求將斷點與查看器寬度斷點匹配。

在響應性設計嵌入模式中，觀看者根據網頁容器的方式不同地工作 `DIV` 大小。 如果網頁僅設定容器的寬度 `DIV`在保持其高度不受限制的情況下，觀看者根據所使用資產的縱橫比自動選擇其高度。 此功能意味著該資產完全適合視圖，而不會在側面出現任何填充。 對於使用響應性設計佈局框架(如Bootstrap和基礎)的網頁，此特定使用案例最常見。

否則，如果網頁為查看者的容器設定寬度和高度 `DIV`，則查看器將僅填充該區域並遵循網頁佈局提供的大小。 一個很好的使用案例示例是將查看器嵌入到模式覆蓋中，其中覆蓋根據Web瀏覽器窗口大小進行大小調整。

**固定大小嵌入**

通過執行以下操作，可將查看器添加到網頁：

1. 將查看器JavaScript檔案添加到網頁。
1. 定義容器 `DIV`。
1. 設定查看器大小。
1. 建立和初始化查看器。

1. 將查看器JavaScript檔案添加到網頁。

   建立查看器要求在HTML頭中添加指令碼標籤。 在使用查看器API之前，請確保包括 `FlyoutViewer.js`。 `FlyoutViewer.js` 在以下 [!DNL html5/js/] 標準IS查看器部署的子資料夾：

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

如果查看器部署在AdobeDynamic Media伺服器之一上，並且從同一域提供服務，則可以使用相對路徑。 否則，您將指定一個AdobeDynamic Media伺服器（安裝了IS-Viewers）的完整路徑。

相對路徑如下所示：

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>僅引用主查看器JavaScript `include` 檔案。 不要引用網頁代碼中任何可能在運行時由查看器邏輯下載的附加JavaScript檔案。 特別是，不直接引用HTML5 SDK `Utils.js` 由查看器從 `/s7viewers` 上下文路徑（所謂統一SDK） `include`)。 原因是 `Utils.js` 或類似的運行時查看器庫由查看器的邏輯和查看器版本之間的位置更改進行完全管理。 Adobe不保留舊版次查看器 `includes` 在伺服器上。
>
>
>因此，直接引用任何輔助JavaScript `include` 該頁面上的查看器使用的瀏覽器功能將在部署新產品版本時中斷查看器功能。

1. 定義容器DIV。

   將空的DIV元素添加到希望查看器顯示的頁面。 DIV元素必須定義其ID，因為此ID稍後會傳遞給查看器API。

   佔位符DIV是定位元素，表示 `position` CSS屬性設定為 `relative` 或 `absolute`。

   指定適當的 `z-index` 。 這樣可確保查看器的彈出部分顯示在其它網頁元素的頂部。

   以下是定義的佔位符DIV元素的示例：

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. 設定查看器大小。

   此查看器在處理多項集時顯示縮略圖。 在案頭系統上，縮略圖放在主視圖下方。 同時，觀看者允許在運行時使用主資產的交換 `setAsset()` API。 作為開發人員，當新資產只有一個項目時，您可以控制查看者如何管理底部區域的縮略圖區域。 可以保持外部查看器大小不變，並讓主視圖增加其高度並佔用縮略圖區域。 或者，您可以保持主視圖大小靜態並折疊外部查看器區域，讓網頁內容向上移動，然後使用縮略圖中剩餘的可用頁面空間。

   要保持外部查看器邊界不變，請定義 `.s7flyoutviewer` 以絕對單位表示的頂級CSS類。 CSS中的大小調整可以放在HTML頁面或自定義查看器CSS檔案中，稍後分配給Dynamic Media Classic的查看器預設記錄，或使用style命令顯式傳遞。

   請參閱 [自定義浮出查看器](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451) 的子菜單。

   以下是在HTML頁中定義靜態外部查看器大小的示例：

   ```html {.line-numbers}
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   您可以在以下示例頁面上看到具有固定外部查看器區域的行為。 請注意，在集之間切換時，外部查看器大小不會改變：

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-outer-area.html)

   要使主視圖尺寸保持靜態，請為內部定義以絕對單位表示的查看器尺寸 `Container` SDK元件使用 `.s7flyoutviewer .s7container` CSS選擇器。 此外，您應覆蓋為 `.s7flyoutviewer` 將預設查看器CSS中的頂級CSS類設定為 `auto`。

   以下是定義內部查看器大小的示例 `Container` SDK元件，以便在切換資產時主視圖區域不更改其大小：

   ```html {.line-numbers}
   #s7viewer.s7flyoutviewer { 
    width: auto; 
    height: auto; 
   }  
   #s7viewer.s7flyoutviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   以下示例頁顯示具有固定主視圖大小的查看器行為。 請注意，在集之間切換時，主視圖保持靜態，網頁內容垂直移動：

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-main-view.html)

   此外，預設查看器CSS為其外部區域提供固定大小。

1. 建立和初始化查看器。

   完成上述步驟後，將建立 `s7viewers.FlyoutViewer` 類，將所有配置資訊傳遞給其建構子和調用 `init()` 的子常式。 配置資訊作為JSON對象傳遞給建構子。 至少，此對象應具有 `containerId` 包含查看器容器ID和嵌套名稱的欄位 `params` JSON對象及其查看器支援的配置參數。 在這個例子中， `params` 對象必須至少將Image Serving URL傳遞為 `serverUrl` 及初始資產 `asset` 的下界。 基於JSON的初始化API允許您使用單行代碼建立和啟動查看器。

   必須將查看器容器添加到DOM中，以便查看器代碼可以通過其ID查找容器元素。 某些瀏覽器將生成DOM延遲到網頁結束。 要獲得最大相容性，請調用 `init()` 方法 `BODY` 標籤，或者身上 `onload()` 的子菜單。

   同時，容器元素還不一定是網頁佈局的一部分。 例如，它可能隱藏在 `display:none` 指定的樣式。 在這種情況下，查看器將其初始化過程延遲到網頁將容器元素帶回佈局的那一刻。 當此操作發生時，查看器載入將自動恢復。

   以下是建立查看器實例的示例，將最小必要配置選項傳遞給建構子，並調用 `init()` 的雙曲餘切值。 該示例假定 `flyoutViewer` 是查看器實例； `s7viewer` 是佔位符的名稱 `DIV`; `http://s7d1.scene7.com/is/image/` 是影像服務URL;和 `Scene7SharedAssets/ImageSet-Views-Sample` 是資產：

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var flyoutViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   以下代碼是嵌入具有固定大小的Flyout查看器的普通網頁的完整示例：

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;z-index:1;"></div> 
   <script type="text/javascript"> 
   var flyoutViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

## 具有無限制高度的響應設計嵌入 {#section-056cb574713c4d07be6d07cf3c598839}

通過響應性設計嵌入，網頁通常具有某種靈活的佈局，其指示查看者容器的運行時大小 `DIV`。 對於以下示例，假定該網頁允許查看者的容器 `DIV` 以取Web瀏覽器窗口大小的40%，使其高度不受限制。 網頁HTML代碼如下所示：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
</style> 
</head> 
<body> 
<div class="holder"></div> 
</body> 
</html>
```

將查看器添加到此頁麵類似於固定大小嵌入的步驟。 唯一的區別是，必須覆蓋預設查看器CSS的固定大小，其大小以相對單位設定。

1. 將查看器JavaScript檔案添加到網頁。
1. 定義容器 `DIV`。
1. 設定查看器大小。
1. 建立和初始化查看器。

以上所有步驟與固定大小嵌入步驟相同，但有以下三個例外：

* 添加容器 `DIV` 持有人」 `DIV`;
* 添加 `imagereload` 具有顯式斷點的參數；
* 不使用絕對單位設定固定查看器大小，而是使用CSS將查看器寬度和高度設定為100%，如下所示：

```html {.line-numbers}
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

以下代碼是一個完整的示例。 注意在調整瀏覽器大小時查看器大小如何變化，以及查看器縱橫比如何與資產匹配。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative;z-index:1"></div> 
</div> 
<script type="text/javascript"> 
var flyoutViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

以下示例頁說明了具有無限制高度的響應設計嵌入在現實生活中的更多用途：

[即時演示](https://landing.adobe.com/tw/na/dynamic-media/ctir-2755/live-demos.html)

[備用演示位置](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

## 定義寬度和高度的柔性尺寸嵌入 {#section-0a329016f9414d199039776645c693de}

如果定義了寬度和高度的靈活大小嵌入，則網頁樣式會有所不同。 它為 `"holder"` DIV並將其居中到瀏覽器窗口中。 此外，網頁還設定 `HTML` 和 `BODY` 元素到100%。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
html, body { 
 width: 100%; 
 height: 100%; 
} 
.holder { 
 position: absolute; 
 left: 20%; 
 top: 20%; 
 width: 60%; 
height: 60%; 
} 
</style> 
</head> 
<body> 
<div class="holder"></div> 
</body> 
</html>
```

其餘嵌入步驟與用於具有無限制高度的響應設計嵌入的步驟相同。 結果示例如下：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
<style type="text/css"> 
html, body { 
 width: 100%; 
 height: 100%; 
} 
.holder { 
 position: absolute; 
 left: 20%; 
 top: 20%; 
 width: 60%; 
height: 60%; 
} 
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative;z-index:1"></div> 
</div> 
<script type="text/javascript"> 
var flyoutViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## 使用基於Setter的API嵌入 {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

可以不使用基於JSON的初始化，而是使用基於setter的API和no-args建構子。 使用此API建構子不採用任何參數，配置參數是使用 `setContainerId()`。 `setParam()`, `setAsset()` API方法，具有單獨的JavaScript調用。

以下示例說明了將固定大小嵌入與基於setter的API一起使用：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7flyoutviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head><body> 
<div id="s7viewer" style="position:relative;z-index:1;"></div> 
<script type="text/javascript"> 
var flyoutViewer = new s7viewers.FlyoutViewer(); 
flyoutViewer.setContainerId("s7viewer"); 
flyoutViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
flyoutViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
flyoutViewer.init(); 
</script> 
</body> 
</html>
```
