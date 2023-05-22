---
title: eCatalog
description: eCatalog Viewer是一個目錄查看器，它按分頁或分頁方式以分頁方式顯示電子手冊。 eCatalog允許用戶使用其他用戶介面元素或專用縮略圖模式在目錄中導航。 用戶還可以放大每頁，以獲得更詳細的資訊。
keywords: 響應
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 8e243fa5-e375-41ce-8b49-2571023130c1
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2160'
ht-degree: 0%

---

# eCatalog{#ecatalog}

eCatalog Viewer是一個目錄查看器，它按分頁或分頁方式以分頁方式顯示電子手冊。 eCatalog允許用戶使用其他用戶介面元素或專用縮略圖模式在目錄中導航。 用戶還可以放大每頁，以獲得更詳細的資訊。

>[!NOTE]
>
>此查看器不支援使用影像渲染(IR)或用戶生成內容(UGC)的影像。

查看器類型507。

請參閱 [系統要求和先決條件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

此查看器可以與對話框配合使用，並支援可選的影像映射和社交共用工具。 它具有縮放工具、目錄導航工具、全屏支援、縮略圖和可選的關閉按鈕。 查看器還支援社交共用工具、打印、下載和收藏夾。 它設計用於台式機和移動設備。

## 演示URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d1.scene7.com/s7viewers/html5/eCatalogViewer.html?asset=Viewers/Pluralist](https://s7d1.scene7.com/s7viewers/html5/eCatalogViewer.html?asset=Viewers/Pluralist)

## 使用eCatalog Viewer {#section-e6c68406ecdc4de781df182bbd8088b4}

eCatalog Viewer表示主JavaScript檔案和一組幫助檔案(單個JavaScript包含該查看器在運行時下載的所有Viewer SDK元件，該查看器由該查看器使用

您可以使用隨IS-Viewer提供的生產就緒型HTML頁或嵌入式模式在彈出模式下使用eCatalog Viewer，在該模式下，使用文檔化的API將其整合到目標網頁中。

配置和外觀與其他查看器類似。 所有蒙皮都是通過自定義CSS實現的。

請參閱 [所有查看器通用的命令引用 — 配置屬性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 和 [所有查看器通用的命令引用 — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 與eCatalog Viewer交互 {#section-642e66ca38cd4032992840ec6c0b0cd2}

eCatalog Viewer支援其他移動應用程式中常見的以下觸控手勢。

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
   <td colname="col2"> <p> 在色板中選擇新的縮略圖。 </p> </td> 
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
   <td colname="col2"> <p> 如果使用幻燈片框架過渡，則滾動目錄頁清單。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直輕掃或輕拂 </p> </td> 
   <td colname="col2"> <p>當影像處於重置狀態時，它執行本機頁面滾動。 </p> <p>當縮略圖處於活動狀態時，它將滾動縮略圖清單。 </p> </td> 
  </tr> 
 </tbody> 
</table>

可以啟用真實的頁面翻轉動畫效果以在目錄頁面之間導航。 在這種情況下，用戶可以按住並拖動頁面角並翻轉頁面。

此查看器還支援Windows設備上的觸摸輸入和滑鼠輸入，並帶有觸摸屏和滑鼠。 但是，此支援僅限於Chrome、Internet Explorer 11和Edge Web瀏覽器。

此查看器可完全按鍵盤訪問，如所述 [鍵盤輔助功能和導航](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 與eCatalog Viewer共用社交媒體工具 {#section-eb575084a99647c3a9591f439f40b412}

eCatalog Viewer支援社交共用工具。 它們可作為主控制欄中的按鈕使用，當用戶按一下或輕擊該按鈕時，該按鈕將擴展為共用工具欄。

共用工具欄包含支援的每種類型共用通道的表徵圖，包括Facebook、Twitter、電子郵件共用、嵌入代碼共用和連結共用。 當激活電子郵件共用、嵌入共用或連結共用工具時，查看器將顯示帶有相應資料輸入表單的模式對話框。 當呼叫Facebook或Twitter時，觀看者將用戶從社會服務重定向到標準共用對話。 由於Web瀏覽器安全限制，共用工具在全屏模式下不可用。

## 嵌入eCatalog查看器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同的網頁對查看者行為有不同的需求。 有時，網頁提供的連結在選中時會在單獨的瀏覽器窗口中開啟查看器。 在其他情況下，必須將查看器右嵌入到托管頁中。 在後一種情況下，該網頁可以具有靜態頁面佈局，或者使用響應設計，該響應設計在不同的設備上顯示不同的或針對不同的瀏覽器窗口大小。 為滿足這些需要，查看器支援三種主要操作模式：彈出式、固定大小嵌入和響應性設計嵌入。

**關於彈出模式**

在彈出模式下，在單獨的Web瀏覽器窗口或頁籤中開啟查看器。 它會佔用整個瀏覽器窗口區域，並在瀏覽器調整大小或移動設備的方向發生變化時進行調整。

彈出模式是移動設備中最常見的模式。 網頁使用 `window.open()` JavaScript調用，正確配置 `A` HTML元件或任何其它合適的方法。

建議您使用現成HTML頁面進行彈出操作模式。 在這種情況下，它叫 [!DNL eCatalogViewer.html] 位於 [!DNL html5/] 標準IS查看器部署的子資料夾：

[!DNL <s7viewers_root>/html5/eCatalogViewer.html]

通過應用自定義CSS，可以實現可視化定製。

以下是在新窗口中開啟查看器的HTML代碼示例：

```html {.line-numbers}
<a href="https://s7d1.scene7.com/s7viewers/html5/eCatalogViewer.html?asset=Viewers/Pluralist" target="_blank">Open popup viewer</a>
```

**關於固定尺寸嵌入模式和響應設計嵌入模式**

在嵌入模式中，查看器被添加到現有網頁中，該網頁可能已經具有與查看器無關的一些客戶內容。 瀏覽者通常只佔用網頁的一部分房地產。

主要使用案例是面向台式機或平板電腦設備的網頁，以及響應性設計的頁面，這些頁面根據設備類型自動調整佈局。

當查看器在初始載入後不更改其大小時，使用固定大小嵌入。 此方法是具有靜態佈局的網頁的最佳選擇。

響應性設計嵌入假定查看器必須在運行時根據其容器的大小變化調整大小 `DIV`。 最常見的用例是向使用靈活頁面佈局的網頁添加查看器。

在響應性設計嵌入模式中，查看器根據網頁大小其容器的方式而具有不同的行為 `DIV`。 如果網頁僅設定容器的寬度 `DIV`在保持高度不受限制的情況下，觀看者根據所使用資產的縱橫比自動選擇其高度。 此功能可確保資產完美地貼入視圖中，而不會在側面出現任何填充。 此使用案例是使用響應性佈局框架(如Bootstrap和Foundation)的網頁中最常見的使用案例。

否則，如果網頁為查看者的容器設定寬度和高度 `DIV`，查看器僅填充該區域並遵循網頁佈局提供的大小。 一個很好的例子是將查看器嵌入到模式覆蓋中，其中覆蓋根據Web瀏覽器窗口大小進行大小調整。

**固定大小嵌入**

通過執行以下操作，可將查看器添加到網頁：

1. 將查看器JavaScript檔案添加到網頁。
1. 定義容器DIV。
1. 設定查看器大小。
1. 建立和初始化查看器。

1. 將查看器JavaScript檔案添加到網頁。

   建立查看器要求在HTML頭中添加指令碼標籤。 在使用查看器API之前，請確保包括 [!DNL eCatalogViewer.js]。 的 [!DNL eCatalogViewer.js] 檔案位於 [!DNL html5/js/] 標準IS查看器部署的子資料夾：

[!DNL <s7viewers_root>/html5/js/eCatalogViewer.js]

如果查看器部署在其中一個Adobe Dynamic Media Classic伺服器上，並且從同一域提供服務，則可以使用相對路徑。 否則，您將指定到安裝了IS-Viewers的Adobe Dynamic Media Classic伺服器之一的完整路徑。

相對路徑如下所示：

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/eCatalogViewer.js"></script>
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

1. 設定查看器大小

   可以通過為聲明查看器來設定其靜態大小 `.s7ecatalogviewer` 頂級CSS類（以絕對單位表示），或使用 `stagesize` 修改量。

   您可以將大小調整直接放在CSS中的HTML頁。 或者，將大小設定在自定義查看器CSS檔案中，該檔案稍後將分配給Dynamic Media Classic的查看器預設記錄，或使用style命令顯式傳遞。

   請參閱 [自定義eCatalog查看器](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) 的子菜單。

   以下是在「HTML」頁中定義靜態查看器大小的示例：

   ```html {.line-numbers}
   #s7viewer.s7ecatalogviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   可以設定 `stagesize` 在Dynamic Media Classic的查看器預設記錄中的修飾符。 或者，可以使用查看器初始化代碼顯式傳遞它， `params` 或作為API調用（如「命令參考」部分中所述），如下所示：

   ```html {.line-numbers}
   eCatalogViewer.setParam("stagesize", 
   "640,480");
   ```

1. 正在初始化查看器。

   完成上述步驟後，將建立 `s7viewers.eCatalogViewer` 類，將所有配置資訊傳遞給其建構子和調用 `init()` 的子常式。 配置資訊作為JSON對象傳遞給建構子。 至少，此對象具有 `containerId` 包含查看器容器ID和嵌套名稱的欄位 `params` 具有查看器支援的配置參數的JSON對象。 在這個例子中， `params` 對象必須至少將Image Serving URL傳遞為 `serverUrl` 及初始資產 `asset` 的下界。 基於JSON的初始化API允許您使用單行代碼建立和啟動查看器。

   必須將查看器容器添加到DOM中，以便查看器代碼可以通過其ID查找容器元素。 某些瀏覽器將生成DOM延遲到網頁結束。 但是，要獲得最大相容性，請調用 `init()` 方法 `BODY` 標籤，或者身上 `onload()` 的子菜單。

   同時，容器元素還不一定是網頁佈局的一部分。 例如，它可能隱藏在 `display:none` 指定的樣式。 在這種情況下，查看器將其初始化過程延遲到網頁將容器元素帶回佈局的那一刻。 當此操作發生時，查看器載入將自動恢復。

   以下是建立查看器實例、將最小必要配置選項傳遞給建構子並調用 `init()` 的雙曲餘切值。 該示例假定 `eCatalogViewer` 是查看器實例； `s7viewer` 是佔位符的名稱 `DIV`; `https://s7d1.scene7.com/is/image/` 是影像服務URL, `Viewers/Pluralist` 是資產：

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var eCatalogViewer = new s7viewers.eCatalogViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"https://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   以下代碼是嵌入固定大小的eCatalog Viewer的普通網頁的完整示例：

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7ecatalogviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var eCatalogViewer = new s7viewers.eCatalogViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"https://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**具有無限制高度的響應設計嵌入**

通過響應性設計嵌入，網頁通常具有某種靈活的佈局，其指示查看者容器的運行時大小 `DIV`。 在本示例中，假定網頁允許查看者的容器 `DIV` 以取Web瀏覽器窗口大小的40%，使其高度不受限制。 生成的網頁HTML代碼如下所示：

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

將查看器添加到此類頁麵類似於固定大小嵌入，唯一的區別是您不需要顯式定義查看器大小。

1. 將查看器JavaScript檔案添加到網頁。
1. 定義容器DIV。
1. 建立和初始化查看器。

上述步驟與固定尺寸嵌入步驟相同。 添加容器 `DIV` 持有人」 `DIV`。 以下代碼是一個完整的示例。 您可以看到在調整瀏覽器大小時查看器大小的變化，以及查看器縱橫比與資產的匹配情況。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
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
var eCatalogViewer = new s7viewers.eCatalogViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

以下示例頁說明了具有無限制高度的響應設計嵌入的更多實際使用案例：

[現場演示](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

**定義寬度和高度的柔性尺寸嵌入**

在定義了寬度和高度的柔性大小嵌入中，網頁樣式是不同的。 即，它為「保持器」提供兩種大小 `DIV` 並將其置於瀏覽器窗口中。 此外，網頁還設定 `HTML` 和 `BODY` 元素到100%:

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

其餘的嵌入步驟與具有無限制高度的響應設計嵌入相同。 結果示例如下：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
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
var eCatalogViewer = new s7viewers.eCatalogViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**使用基於Setter的API嵌入**

可以不使用基於JSON的初始化，而是使用基於setter的API和no-args建構子。 使用該API建構子不使用任何參數，配置參數是使用 `setContainerId()`。 `setParam()`, `setAsset()` API方法，具有單獨的JavaScript調用。

以下示例顯示使用基於setter的API的固定大小嵌入：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7ecatalogviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var eCatalogViewer = new s7viewers.eCatalogViewer(); 
eCatalogViewer.setContainerId("s7viewer"); 
eCatalogViewer.setParam("serverurl", "https://s7d1.scene7.com/is/image/"); 
eCatalogViewer.setAsset("Viewers/Pluralist"); 
eCatalogViewer.init(); 
</script> 
</body> 
</html>
```
