---
title: 全景查看器
description: HTML5全景查看器是顯示全景影像的影像查看器。 該觀看器的目的是顯示球面全景圖，也稱為等長形影像。 它通過陀螺運動支援自動平移和平移。 它設計用於台式機和移動設備。 在支援移動設備上提供虛擬現實觀看模式。
keywords: 響應
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '1953'
ht-degree: 0%

---

# 全景{#panoramic}

HTML5全景查看器是顯示全景影像的影像查看器。 該觀看器的目的是顯示球面全景圖，也稱為等長形影像。 它通過陀螺運動支援自動平移和平移。 它設計用於台式機和移動設備。 在支援移動設備上提供虛擬現實觀看模式。

請參閱 [系統要求和先決條件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。


查看器類型514。

## 演示URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample](http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample)

## 使用全景查看器 {#section-f21ac23d3f6449ad9765588d69584772}

HTML5全景查看器表示主JavaScript檔案和查看器在運行時下載的幫助檔案集。 幫助檔案集是一個JavaScript，包含此特定查看器、資產、CSS使用的所有HTML5查看器SDK元件。
HTML5全景查看器既可以在彈出模式下使用隨IS查看器提供的生產就緒HTML頁，也可以在嵌入式模式下使用文檔化的API將其整合到目標網頁中。
配置和外觀與其他HTML5查看器的配置和外觀相似。 所有蒙皮可通過自定義CSS實現。

請參閱 [所有查看器通用的命令引用 — 配置屬性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 和 [所有查看器通用的命令引用 — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 與HTML5全景查看器交互 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

HTML5全景查看器支援通過拖動或陀螺儀移動進行自動平移和導航。

<table id="table_panoramic"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>導覽 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>桌上型電腦 </p> </td> 
   <td colname="col2"> <p>自動平移和拖動以導航。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>觸摸裝置 </p> </td> 
   <td colname="col2"> <p>預設情況下，自動平移和拖動以導航。 在VR渲染模式下通過陀螺儀移動導航(vrrender=true)。
 </p> </td> 
  </tr> 
 </tbody> 
</table>

查看器支援Windows設備上的觸摸輸入和滑鼠輸入，並帶有觸摸屏和滑鼠，但僅限於Chrome、Internet Explorer 11和Edge Web瀏覽器。
全景查看器可以通過指定vrrender修飾符在虛擬現實(VR)模式下呈現全景影像。 啟用vrrender後，全景影像會顯示在分割的螢幕中。 通用用例是在安裝在虛擬現實耳機中的行動電話中提供影像，為每隻眼睛提供單獨的影像。 觀看者響應頭部的陀螺運動並瀏覽影像。

## 嵌入HTML5全景查看器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同的網頁對查看者行為有不同的需求。 有時網頁提供連結。 選擇該連結將在單獨的瀏覽器窗口中開啟查看器。 在其它情況下，可能需要將查看器嵌入到托管頁面中。 在後一種情況下，網頁可以具有靜態佈局，或者是「響應」的，並且在不同的設備上或不同的瀏覽器窗口大小顯示不同。 為滿足這些需要，查看器支援三種主要操作模式：彈出窗口、固定大小嵌入和響應性嵌入。

**關於彈出模式**

在彈出模式中，查看器在單獨的Web瀏覽器窗口或頁籤中開啟。 它取整個瀏覽器窗口區域，在瀏覽器調整大小或設備方向改變時進行調整。

此模式是移動設備中最常見的模式。 網頁使用 `window.open()` JavaScript調用、正確配置HTML元素或任何其他合適的方法。

建議您使用現成HTML頁面進行彈出操作模式。 它叫 [!DNL PanoramicViewer.html] 它位於 [!DNL html5/] 標準IS查看器部署的子資料夾：

[!DNL <s7viewers_root>/html5/PanoramicViewer.html]

通過應用自定義CSS實現可視化定製。

下面是HTML代碼的示例，該代碼在新窗口中開啟查看器：

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample" target="_blank">Open popup viewer</a>
```

**關於固定尺寸嵌入模式和響應嵌入模式**

在嵌入式模式下，查看器被添加到現有網頁中，該網頁可能已經具有與查看器無關的一些客戶內容。 瀏覽器通常只佔網頁房地產的一部分。

主要使用案例是面向台式機或平板電腦設備的網頁，以及響應性網頁，這些網頁根據設備類型自動調整佈局。

在初始載入後查看器不更改其大小時，使用固定大小嵌入。 該方法是靜態佈局網頁的最佳選擇。

響應嵌入假定查看器必須在運行時調整大小以響應其容器DIV的大小變化。 最常見的用例是向使用靈活佈局的網頁添加查看器。

在響應模式下，查看器根據網頁大小其容器DIV的方式而具有不同的行為。 如果網頁僅設定容器DIV的寬度，而保持其高度不受限制，則查看者根據所使用資產的長寬比自動選擇其高度。 該方法確保該資產完美地適合於視圖，而不會在側面產生任何填充。 此使用案例是使用響應性佈局框架(如Bootstrap、基礎等)的網頁中最常見的使用案例。

否則，如果網頁為查看器的容器DIV設定寬度和高度，則查看器將填充該區域並遵循網頁佈局提供的大小。 一個很好的例子是將查看器嵌入到模式覆蓋中，其中覆蓋根據Web瀏覽器窗口大小進行大小調整。

**固定大小嵌入**

通過執行以下操作，可將查看器添加到網頁：

1. 將查看器JavaScript檔案添加到網頁。
1. 定義容器 `DIV`。
1. 設定查看器大小。
1. 建立和初始化查看器。

1. 將查看器JavaScript檔案添加到網頁。

   建立查看器要求在HTML頭中添加指令碼標籤。 在使用查看器API之前，請確保包括 [!DNL PanoramicViewer.js]。 的 [!DNL PanoramicViewer.js] 檔案位於 [!DNL html5/js/] 標準IS查看器部署的子資料夾：

[!DNL <s7viewers_root>/html5/js/PanoramicViewer.js]

如果查看器部署在其中一個Adobe Dynamic Media Classic伺服器上，並且從同一域提供服務，則可以使用相對路徑。 否則，您將指定到安裝了IS-Viewers的Adobe Dynamic Media Classic伺服器之一的完整路徑。

相對路徑如下所示：

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/PanoramicViewer.js"></script>
```

>[!NOTE]
>
>僅引用主查看器JavaScript `include` 檔案。 不要引用網頁代碼中任何可能在運行時由查看器邏輯下載的附加JavaScript檔案。 特別是，不直接引用HTML5 SDK `Utils.js` 由查看器從 `/s7viewers` 上下文路徑（所謂統一SDK） `include`)。 原因是 `Utils.js` 或類似的運行時查看器庫由查看器的邏輯和查看器版本之間的位置更改進行完全管理。 Adobe不保留舊版次查看器 `includes` 在伺服器上。
>
>
>因此，直接引用任何輔助JavaScript `include` 該頁面上的查看器使用的瀏覽器功能將在部署新產品版本時中斷查看器功能。

1. 定義容器DIV。

   將空的DIV元素添加到希望查看器顯示的頁面。 DIV元素必須定義其ID，因為此ID稍後會傳遞給查看器API。 DIV的大小通過CSS指定。

   佔位符DIV是定位元素，表示 `position` CSS屬性設定為 `relative` 或 `absolute`。


   以下是定義的佔位符DIV元素的示例：

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. 設定查看器大小

   可以通過為聲明查看器來設定其靜態大小 `.s7panoramicviewer` 頂級CSS類（以絕對單位表示），或使用修飾符 `stagesize`。

   CSS中的大小調整可以放在HTML頁或自定義查看器CSS檔案中，該檔案稍後將分配給AOD中的查看器預設記錄，或使用style命令顯式傳遞。 有關使用CSS設定查看器樣式的詳細資訊，請參閱「自定義查看器」部分。 下面是在HTML頁中定義靜態查看器大小的示例：

   ```html {.line-numbers}
   #s7viewer.s7panoramicviewer {
     width: 1024px;
     height: 512px;
   }
   ```

   `stagesize` 修飾符可以與帶有params集合的查看器初始化代碼一起顯式傳遞，也可以作為API調用（如「命令參考」部分所述），如下所示：

   ```html {.line-numbers}
   panoramicViewer.setParam("stagesize", "512,256");
   ```

   建議使用基於CSS的方法，並在本示例中使用。

1. 建立和初始化查看器。

   完成上述步驟後，將建立 `s7viewers.PanoramicViewer` 類，將所有配置資訊傳遞給其建構子和調用 `init(`)方法。 配置資訊作為JSON對象傳遞給建構子。 至少，此對象應具有containerId欄位，該欄位包含查看器容器ID的名稱和嵌套參數JSON對象，並且查看器支援配置參數。 在這種情況下，params對象必須至少將Image Serving URL傳遞為 `serverUrl` 屬性和初始資產作為資產參數。 基於JSON的初始化API允許您使用單行代碼建立和啟動查看器。

   必須將查看器容器添加到DOM中，以便查看器代碼可以通過其ID查找容器元素。 某些瀏覽器將生成DOM延遲到網頁結束。 要獲得最大相容性，請調用 `init()` 方法 `BODY` 標籤，或者身上 `onload()` 的子菜單。

   同時，容器元素還不一定是網頁佈局的一部分。 例如，它可能隱藏在 `display:none` 指定的樣式。 在這種情況下，查看器將其初始化過程延遲到網頁將容器元素帶回佈局的那一刻。 當此操作發生時，查看器載入將自動恢復。

   以下是建立查看器實例、將最小必要配置選項傳遞給建構子並調用 `init()` 的雙曲餘切值。 此示例假定 `panoramicViewer` 是查看器實例， `s7viewer` 是佔位符的名稱 `DIV`。 [!DNL http://s7d1.scene7.com/is/image/] 是影像服務URL, [!DNL Scene7SharedAssets/PanoramicImage-Sample] 是資產。

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var panoramicViewer = new s7viewers.PanoramicViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
     "asset":"Scene7SharedAssets/PanoramicImage-Sample",
     "serverurl":"http://s7d1.scene7.com/is/image/"
   } 
   }).init(); 
   </script> 
   ```

   下面的代碼是一個簡單網頁的完整示例，該網頁嵌入了具有固定大小的全景查看器：

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
    <head>
    <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
    <style type="text/css">
    #s7viewer.s7panoramicviewer {
        width: 1024px;
        height: 512px;
    }
    </style>
    </head>
    <body>
    <div id="s7viewer" style="position:relative"></div>
    <script type="text/javascript">
    var panoramicViewer = new s7viewers.PanoramicViewer({
        "containerId":"s7viewer",
    "params":{
        "asset":"Scene7SharedAssets/PanoramicImage-Sample",
        "serverurl":"http://s7d1.scene7.com/is/image/"
    }
    }).init();
    </script>
    </body>
    </html>
   ```

**具有無限制高度的響應設計嵌入**

通過響應嵌入，網頁通常具有某種靈活的佈局，這決定了觀看者的容器DIV的運行時間大小。 在本示例中，我們假設該網頁允許查看者的容器DIV佔用Web瀏覽器窗口大小的80%，而保持其高度不受限制。 網頁HTML代碼可能如下所示：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
.holder {
	width: 80%;
}
</style>
</head>
<body>
<div class="holder"></div>
</body>
</html> 
```

將查看器添加到此頁麵類似於固定大小嵌入，唯一的區別是您不需要顯式定義查看器大小：

1. 將查看器JavaScript檔案添加到網頁。
1. 定義容器DIV。
1. 建立和初始化查看器。

上述步驟與固定尺寸嵌入步驟相同。 應將容器DIV添加到現有「保持器」DIV。 以下代碼是一個完整的示例，您可以看到調整瀏覽器大小時查看器大小的變化，以及查看器縱橫比與資產的匹配情況。

```html {.line-numbers}
<!DOCTYPE html>
<html>
<head>
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
<style type="text/css">
.holder {
	width: 80%;
}
</style>
</head>
<body>
<div class="holder">
<div id="s7viewer" style="position:relative"></div>
</div>
<script type="text/javascript">
var panoramicViewer = new s7viewers.PanoramicViewer({
	"containerId":"s7viewer",
"params":{
	"asset":"Scene7SharedAssets/PanoramicImage-Sample",
	"serverurl":"http://s7d1.scene7.com/is/image/"
}
}).init();
</script>
</body>
</html>
```

以下示例頁說明了在不受限制高度的情況下更真實地使用響應性設計嵌入：

[即時演示](https://landing.adobe.com/tw/na/dynamic-media/ctir-2755/live-demos.html)

[備用演示位置](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**定義寬度和高度的響應設計嵌入**

如果有響應性設計嵌入，定義了寬度和高度，則網頁的造型方式不同；它為「保持器」提供兩種大小 `DIV` 並在瀏覽器窗口中居中。 此外，網頁還設定 `HTML` 和 `BODY` 元素到100%:

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

其餘的嵌入步驟與具有無限制高度的響應嵌入相同。 結果示例是

```html {.line-numbers}
<!DOCTYPE html>
<html>
<head>
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
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
var panoramicViewer = new s7viewers.PanoramicViewer({
	"containerId":"s7viewer",
"params":{
	"asset":"Scene7SharedAssets/PanoramicImage-Sample",
	"serverurl":"http://s7d1.scene7.com/is/image/"
}
}).init();
</script>
</body>
</html>
```

**使用基於Setter的API嵌入**

可以不使用基於JSON的初始化，而是使用基於setter的API和no-args建構子。 使用該API，建構子不採用任何參數，並且配置參數是使用 `setContainerId()`。 `setParam()`, `setAsset()` API方法，具有單獨的JavaScript調用。

以下示例說明了使用基於setter的API進行固定大小嵌入的過程：

```html {.line-numbers}
<!DOCTYPE html>
<html>
<head>
<script language="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
<style type="text/css">
#s7viewer.s7panoramicviewer {
	width: 1024;
	height: 512;
}
</style>
</head>
<body>
<div id="s7viewer" style="position:relative"></div>
<script type="text/javascript">
var panoramicViewer = new s7viewers.PanoramicViewer();
panoramicViewer.setContainerId("s7viewer");
panoramicViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/");
panoramicViewer.setAsset("Scene7SharedAssets/PanoramicImage-Sample");
panoramicViewer.init();
</script>
</body>
</html>
```
