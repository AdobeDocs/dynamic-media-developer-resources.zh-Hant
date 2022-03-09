---
title: Zoom
description: 縮放查看器是顯示可縮放影像的影像查看器。 此查看器可與影像集配合使用，並使用色板完成導航。 它具有縮放工具、全屏支援、色板和可選的關閉按鈕。 它設計用於台式機和移動設備。
keywords: 響應
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 81a74026-fb15-4f57-a4c7-1ab005950245
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2395'
ht-degree: 0%

---

# 縮放{#zoom}

縮放查看器是顯示可縮放影像的影像查看器。 此查看器可與影像集配合使用，並使用色板完成導航。 它具有縮放工具、全屏支援、色板和可選的關閉按鈕。 它設計用於台式機和移動設備。

>[!NOTE]
>
>此查看器不支援使用IR（影像呈現）或UGC（用戶生成的內容）的影像。

查看器類型502。

請參閱 [系統要求和先決條件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

## 演示URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## 使用縮放查看器 {#section-e6c68406ecdc4de781df182bbd8088b4}

縮放查看器表示主JavaScript檔案和一組幫助檔案（單個JavaScript包含該查看器在運行時下載的所有查看器SDK元件，該查看器由此特定查看器、資產和CSS使用）。

可以使用隨IS-Viewers提供的生產就緒型HTML頁或嵌入式模式在彈出模式下使用縮放查看器，在該模式下，使用文檔化的API將縮放查看器整合到目標網頁中。

配置和外觀與其他查看器類似。 所有蒙皮都是通過自定義CSS實現的。

請參閱 [所有查看器通用的命令引用 — 配置屬性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 和 [所有查看器通用的命令引用 — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 與縮放查看器交互 {#section-642e66ca38cd4032992840ec6c0b0cd2}

縮放查看器支援以下在其他移動應用程式中常見的觸控手勢。 當查看器無法處理用戶的刷新手勢時，它會將事件轉發到Web瀏覽器以執行本機頁面滾動。 即使查看器佔據設備螢幕區域的大部分，用戶也可以通過這種功能瀏覽頁面。

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
   <td colname="col2"> <p> 在色板中選擇新的縮略圖。 在主視圖中，它隱藏或顯示用戶介面元素。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>按兩下 </p> </td> 
   <td colname="col2"> <p> 縮放一個級別，直到達到最大放大率。 下一個按兩下手勢將查看器重置為初始查看狀態。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>捏 </p> </td> 
   <td colname="col2"> <p>放大或縮小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>水準輕掃或輕拂 </p> </td> 
   <td colname="col2"> <p> 在色板欄中滾動色板清單。 </p> <p> 如果影像處於重置狀態，並且 <span class="codeph"> 框架過渡 </span> 參數設定為slide，資產隨幻燈片動畫一起更改。 其他 <span class="codeph"> 框架過渡 </span> 模式，該手勢執行本機頁面滾動。 </p> <p> 如果放大影像，則影像會水準移動。 如果影像被移動到視圖邊緣並且沿相同方向執行刷掃，則該手勢執行本地頁面滾動。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直滑動 </p> </td> 
   <td colname="col2"> <p> 如果影像處於重置狀態，則手勢執行本機頁滾動。 </p> <p> 放大影像後，影像將垂直移動。 如果影像被移動到視圖邊緣並且沿相同方向執行滑動，則手勢執行本地頁面滾動。 </p> <p> 如果手勢是在色板區域內完成的，則它將執行本機頁面滾動。 </p> </td> 
  </tr> 
 </tbody> 
</table>

該查看器支援Windows設備上的觸摸輸入和滑鼠輸入，並帶有觸摸屏和滑鼠。 但是，此支援僅限於Chrome、Internet Explorer 11和Edge Web瀏覽器。

此查看器可完全以鍵盤方式訪問。

請參閱 [鍵盤輔助功能和導航](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 嵌入縮放查看器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同的網頁對查看者行為有不同的需求。 有時，網頁提供的連結在選中時會在單獨的瀏覽器窗口中開啟查看器。 在其他情況下，需要將查看器直接嵌入到托管頁面中。 在後一種情況下，網頁可具有靜態佈局，或使用響應設計，該響應設計在不同的設備上顯示不同或對於不同的瀏覽器窗口大小顯示不同。 為滿足這些需要，查看器支援三種主要操作模式：彈出式、固定大小嵌入和響應性設計嵌入。

**關於彈出模式**

在彈出模式下，在單獨的Web瀏覽器窗口或頁籤中開啟查看器。 它會佔用整個瀏覽器窗口區域，並在瀏覽器調整大小或設備方向發生變化時進行調整。

此模式是移動設備中最常見的模式。 網頁使用 `window.open()` JavaScript調用，正確配置 `A` HTML元件或任何其它合適的方法。

建議您使用彈出式操作模式的出廠HTML頁。 現成HTML頁稱為 `ZoomViewer.html` 它位於 `html5/` 標準IS-Viewers部署的子資料夾，如下所示：

`<s7viewers_root>/html5/ZoomViewer.html`

應用自定義CSS以實現頁面的自定義外觀。

以下是在新窗口中開啟查看器的HTML代碼示例：

```html {.line-numbers}
 <a href="http://s7d1.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample" 
target="_blank">Open popup viewer</a>
```

**關於固定尺寸嵌入模式和響應設計嵌入模式**

在嵌入式模式下，查看器被添加到現有網頁中，該網頁可能已經具有與查看器無關的一些客戶內容。 瀏覽者通常只佔據網頁的一部分房地產。

主要使用案例是面向台式機或平板電腦設備的網頁，以及響應性設計的頁面，根據設備類型自動調整佈局。

當查看器在初始載入後不更改其大小時，使用固定大小嵌入。 此選項是具有靜態佈局的網頁的最佳選擇。

響應性設計嵌入模式假定在運行時由於容器的大小變化而需要調整查看器的大小 `DIV`。 最常見的用例是向使用靈活佈局的網頁添加查看器。

在響應性設計嵌入模式中，查看器根據網頁大小其容器的方式而具有不同的行為 `DIV`。 如果網頁僅設定容器的寬度 `DIV`在保持高度不受限制的情況下，觀看者根據所使用資產的縱橫比自動選擇其高度。 這一邏輯確保資產完美地貼入視圖中，而不會在側面出現任何填充。 對於使用響應性佈局框架(如Bootstrap和基礎)的網頁，此使用案例最常見。

如果網頁為查看者的容器設定寬度和高度 `DIV`，查看器將填充該區域並遵循網頁提供的大小。 例如，將查看器嵌入到模式覆蓋中，其中覆蓋根據Web瀏覽器窗口大小進行大小調整。

## 固定大小嵌入 {#section-44f365e6c0dd40709467a459afa82a7f}

通過執行以下操作，可將查看器添加到網頁：

1. 將查看器JavaScript檔案添加到網頁。
1. 定義容器DIV。
1. 設定查看器大小。
1. 建立和初始化查看器。

1. 將查看器JavaScript檔案添加到網頁。

   建立查看器要求在HTML頭中添加指令碼標籤。 在使用查看器API之前，請確保包括 [!DNL ZoomViewer.js]。 的 [!DNL ZoomViewer.js] 檔案位於 [!DNL html5/js/] 標準IS查看器部署的子資料夾：

[!DNL <s7viewers_root>/html5/js/ZoomViewer.js]

如果查看器部署在其中一個Adobe Dynamic Media Classic伺服器上，並且從同一域提供服務，則可以使用相對路徑。 否則，您將指定到安裝了IS-Viewers的Adobe Dynamic Media Classic伺服器之一的完整路徑。

相對路徑如下所示：

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/ZoomViewer.js"></script>
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

   以下是定義的佔位符DIV元素的示例：

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. 設定查看器大小。

   此查看器在處理多項目集時顯示縮略圖，在案頭系統上，縮略圖放在主視圖下方。 同時，查看器允許在運行時使用 `setAsset()` API。 作為開發人員，您可以控制當新資產只有一個項目時查看者如何管理底部的縮略圖區域。 可以保持外部查看器大小不變，並讓主視圖增加其高度並佔用縮略圖區域。 或者，您可以保持主視圖大小靜態並折疊外部查看器區域，讓網頁內容向上移動，並使用縮略圖中剩餘的免費螢幕房地產。

   要保持外部查看器邊界不變，請定義 `.s7zoomviewer` 以絕對單位表示的頂級CSS類。 CSS中的大小調整可以放在HTML頁上。 或者，它可以放在自定義查看器CSS檔案中，該檔案稍後會分配給Dynamic Media Classic的查看器預設記錄，或使用style命令顯式傳遞。

   請參閱 [自定義縮放查看器](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-customizingviewer/c-html5-20-zoom-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) 的子菜單。

   以下是在「HTML」頁中定義靜態外部查看器大小的示例：

   ```html {.line-numbers}
   #s7viewer.s7zoomviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   在以下示例中，可使用固定外部查看器查看行為。 請注意，在集之間切換時，外部查看器大小不會改變：

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-outer-area.html)

   要使主視圖尺寸保持靜態，請為內部定義以絕對單位表示的查看器尺寸 `Container` 使用 `.s7zoomviewer` `.s7container` CSS選擇器，或使用 `stagesize` 修改量。

   以下是定義內部查看器大小的示例 `Container` SDK元件，以便在切換資產時主視圖區域不更改其大小：

   ```html {.line-numbers}
   #s7viewer.s7zoomviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   以下演示頁顯示具有固定主視圖大小的查看器行為。 請注意，在集之間切換時，主視圖保持靜態，網頁內容垂直移動。

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-main-view.html)

   可以設定 `stagesize` 在Dynamic Media Classic的查看器預設記錄中的修飾符。 或者，可以使用查看器初始化代碼將其顯式 `params` 或作為API調用（如本幫助的「命令參考」部分中所述），如下所示：

   ```html {.line-numbers}
    zoomViewer.setParam("stagesize", 
   "640,480");
   ```

   建議使用基於CSS的方法，並在本示例中使用。

1. 建立和初始化查看器。

   完成上述步驟後，將建立 `s7viewers.ZoomViewer` 類，將所有配置資訊傳遞給其建構子和調用 `init()` 的子常式。

   配置資訊作為JSON對象傳遞給建構子。 至少，此對象應 `containerId` 包含查看器容器ID名稱和嵌套的欄位 `params` JSON對象及其查看器支援的配置參數。 在這個例子中， `params` 對象必須至少將Image Serving URL傳遞為 `serverUrl` 及初始資產 `asset` 的下界。 基於JSON的初始化API允許您使用單行代碼建立和啟動查看器。

   必須將查看器容器添加到DOM中，以便查看器代碼可以通過其ID查找容器元素。 某些瀏覽器將生成DOM延遲到網頁結束。 要獲得最大相容性，請調用 `init()` 方法 `BODY` 標籤，或者身上 `onload()` 的子菜單。

   同時，容器元素還不一定是網頁佈局的一部分。 例如，它可能隱藏在 `display:none` 指定的樣式。 在這種情況下，查看器將其初始化過程延遲到網頁將容器元素帶回佈局的那一刻。 當此操作發生時，查看器載入將自動恢復。

   以下是建立查看器實例、將最小必要配置選項傳遞給建構子並調用 `init()` 的雙曲餘切值。 此示例假定 `zoomViewer` 是查看器實例， `s7viewer` 是佔位符DIV的名稱， `http://s7d1.scene7.com/is/image/` 是影像服務URL, `Scene7SharedAssets/ImageSet-Views-Sample` 是資產。

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var zoomViewer = new s7viewers.ZoomViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   下面的代碼是一個簡單網頁的完整示例，該網頁嵌入了固定大小的視頻查看器：

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7zoomviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var zoomViewer = new s7viewers.ZoomViewer({ 
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

## 具有無限制高度的響應設計嵌入 {#section-b9ca11a7e7aa4f74ab43244cbca37ae0}

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

將查看器添加到此頁麵類似於固定大小嵌入的步驟。 唯一的區別是您不需要顯式定義查看器大小。

1. 將查看器JavaScript檔案添加到網頁。
1. 定義容器DIV。
1. 建立和初始化查看器。

上述步驟與固定尺寸嵌入步驟相同。 將容器DIV添加到現有 `"holder"` DIV 以下代碼是一個完整的示例。 注意當瀏覽器調整大小時查看器大小如何變化，以及查看器縱橫比如何匹配資產。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative"></div> 
</div> 
<script type="text/javascript"> 
var zoomViewer = new s7viewers.ZoomViewer({ 
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

以下示例頁說明了具有無限制高度的響應設計嵌入在現實生活中的更多用途：

[現場演示](https://landing.adobe.com/tw/na/dynamic-media/ctir-2755/live-demos.html)

## 定義寬度和高度的柔性尺寸嵌入 {#section-3674e6c032594441a6576b7fb1de6e64}

如果定義了寬度和高度的靈活大小嵌入，則網頁樣式會有所不同。 它為 `"holder"` DIV並將其置於瀏覽器窗口中。 此外，網頁還設定 `HTML` 和 `BODY` 元素到100%。

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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
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
<div class="holder"> 
<div id="s7viewer" style="position:relative"></div> 
</div> 
<script type="text/javascript"> 
var zoomViewer = new s7viewers.ZoomViewer({ 
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

## 使用基於setter的API嵌入 {#section-44e014925f24418b900696003855c0a9}

可以不使用基於JSON的初始化，而是使用基於setter的API和no-args建構子。 使用此API建構子不採用任何參數，配置參數是使用 `setContainerId()`。 `setParam()`, `setAsset()` API方法，具有單獨的JavaScript調用。

以下示例說明了將固定大小嵌入與基於setter的API一起使用：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7zoomviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var zoomViewer = new s7viewers.ZoomViewer(); 
zoomViewer.setContainerId("s7viewer"); 
zoomViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
zoomViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
zoomViewer.init(); 
</script> 
</body> 
</html> 
```
