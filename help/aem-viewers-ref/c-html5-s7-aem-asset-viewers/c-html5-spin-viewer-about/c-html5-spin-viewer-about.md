---
title: Spin
description: 旋轉查看器是一個影像查看器，它提供了360度的影像視圖，甚至是多維視圖（如果正使用適當的旋轉集）。 它具有縮放和旋轉工具、全屏支援和可選的關閉按鈕。 它設計用於台式機和移動設備。
keywords: 響應
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 4c802d42-ea5b-4f28-b6ef-2689aa16839d
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2130'
ht-degree: 0%

---

# Spin{#spin}

旋轉查看器是一個影像查看器，它提供了360度的影像視圖，甚至是多維視圖（如果正使用適當的旋轉集）。 它具有縮放和旋轉工具、全屏支援和可選的關閉按鈕。 它設計用於台式機和移動設備。

>[!NOTE]
>
>此查看器不支援使用IR（影像呈現）或UGC（用戶生成的內容）的影像。

查看器類型503。

請參閱 [系統要求和先決條件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

## 演示URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&amp;stagesize=500,400](https://s7d9.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&amp;stagesize=500,400)

## 使用旋轉查看器 {#section-e6c68406ecdc4de781df182bbd8088b4}

Spin Viewer表示主JavaScript檔案和一組幫助檔案（單個JavaScript包含該查看器在運行時下載的所有Viewer SDK元件，該查看器由該查看器所使用的特定查看器、資產和CSS）。

Spin Viewer既可以使用隨IS-Viewer提供的生產就緒HTML頁在彈出模式下使用，也可以在嵌入式模式下使用，在該模式下，它使用文檔化的API整合到目標網頁中。

配置和外觀與其他查看器類似。 所有蒙皮可通過自定義CSS實現。

請參閱 [所有查看器通用的命令引用 — 配置屬性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 和 [所有查看器通用的命令引用 — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 與旋轉查看器交互 {#section-642e66ca38cd4032992840ec6c0b0cd2}

Spin Viewer支援以下在其他移動應用程式中常見的觸控手勢。 當查看器無法處理用戶的刷卡手勢時，它會將事件轉發到Web瀏覽器以執行本機頁面滾動。 此功能允許用戶在頁面中導航，即使查看器佔據了大部分設備螢幕區域。

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>手勢 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>按兩下 </p> </td> 
   <td colname="col2"> <p> 縮放一個級別，直到達到最大放大率。 下一個按兩下手勢將查看器重置為初始查看狀態。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>捏 </p> </td> 
   <td colname="col2"> <p>放大或縮小影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>水準輕掃或輕拂 </p> </td> 
   <td colname="col2"> <p> 如果影像處於重置狀態，則影像會水準旋轉設定。 </p> <p> 如果放大影像，則影像會水準移動。 如果影像被移動到視圖邊緣並且仍然沿該方向進行輕掃，則手勢執行本機頁面滾動。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直輕掃或輕拂 </p> </td> 
   <td colname="col2"> <p> 如果影像處於重置狀態，則當使用多維自旋集時，它改變垂直視角。 在一維旋轉集中，該手勢執行本機頁滾動。 或者，當多維旋轉集位於最後一個或第一個軸上以使得垂直滑動不會導致垂直視圖角度改變時，該手勢還執行本機頁面滾動。 </p> <p> 如果放大影像，則影像將垂直移動。 如果影像被移動到視圖邊緣並且仍然沿該方向進行輕掃，則手勢執行本機頁面滾動。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>該查看器還支援Windows設備上的觸摸屏和滑鼠輸入。 但是，此支援僅限於Chrome、Internet Explorer 11和Edge Web瀏覽器。

此查看器可完全以鍵盤方式訪問。

請參閱 [鍵盤輔助功能和導航](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 嵌入旋轉查看器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同的網頁對查看者行為有不同的需求。 有時，網頁提供的連結在選中時會在單獨的瀏覽器窗口中開啟查看器。 在其他情況下，必須將查看器右嵌入到托管頁中。 在後一種情況下，該網頁可以具有靜態頁面佈局，或者使用響應設計，該響應設計在不同的設備上顯示不同的或針對不同的瀏覽器窗口大小。 為滿足這些需要，查看器支援三種主要操作模式：彈出式、固定大小嵌入和響應性設計嵌入。

**關於彈出模式**

在彈出模式下，在單獨的Web瀏覽器窗口或頁籤中開啟查看器。 它會佔用整個瀏覽器窗口區域，並在瀏覽器調整大小或移動設備的方向發生變化時進行調整。

彈出模式是移動設備中最常見的模式。 網頁使用 `window.open()` JavaScript調用，正確配置 `A` HTML元件或任何其它合適的方法。

建議您使用現成HTML頁面進行彈出操作模式。 在這種情況下，它叫 [!DNL SpinViewer.html] 位於 [!DNL html5/] 標準IS查看器部署的子資料夾：

[!DNL <s7viewers_root>/html5/SpinViewer.html]

通過應用自定義CSS，可以實現可視化定製。

以下是在新窗口中開啟查看器的HTML代碼示例：

```html {.line-numbers}
<a href="https://s7d1.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&stagesize=500,400" 
target="_blank">Open popup viewer</a>
```

**關於固定尺寸嵌入模式和響應設計嵌入模式**

在嵌入模式中，查看器被添加到現有網頁中，該網頁可能已經具有與查看器無關的一些客戶內容。 瀏覽者通常只佔用網頁的一部分房地產。

主要使用案例是面向台式機或平板電腦設備的網頁，還有響應性設計頁面，根據設備類型自動調整佈局。

當查看器在初始載入後不更改其大小時，使用固定大小嵌入。 此操作是具有靜態佈局的網頁的最佳選擇。

響應性設計嵌入假定查看器必須在運行時根據其容器的大小變化調整大小 `DIV`。 最常見的用例是向使用靈活頁面佈局的網頁添加查看器。

在響應性設計嵌入模式中，查看器根據網頁大小其容器的方式而具有不同的行為 `DIV`。 如果網頁僅設定容器的寬度 `DIV`在保持高度不受限制的情況下，觀看者根據所使用資產的縱橫比自動選擇其高度。 此功能可確保資產完美地貼入視圖中，而不會在側面出現任何填充。 此使用案例是使用響應性設計佈局框架(如Bootstrap或Foundation)的網頁中最常見的使用案例。

否則，如果網頁為查看者的容器設定寬度和高度 `DIV`，查看器僅填充該區域並遵循網頁佈局提供的大小。 一個好的示例是將查看器嵌入到模式覆蓋中，其中覆蓋根據Web瀏覽器窗口大小進行大小調整。

**固定大小嵌入**

通過執行以下操作，可以將Spin Viewer添加到網頁：

1. 將查看器JavaScript檔案添加到網頁。
1. 定義容器 `DIV`。
1. 設定查看器大小。
1. 建立和初始化查看器。

1. 將查看器JavaScript檔案添加到網頁。

   建立查看器要求在HTML頭中添加指令碼標籤。 在使用查看器API之前，請確保包括 `SpinViewer.js`。 `SpinViewer.js` 位於 [!DNL html5/js/] 標準IS查看器部署的子資料夾：

   `<s7viewers_root>/html5/js/SpinViewer.js`

   如果查看器部署在AdobeDynamic Media伺服器之一上，並且從同一域提供服務，則可以使用相對路徑。 否則，您將指定一個AdobeDynamic Media伺服器（安裝了IS-Viewers）的完整路徑。

   相對路徑如下所示：

   ```html {.line-numbers}
    <script language="javascript" type="text/javascript" src="/s7viewers/html5/js/SpinViewer.js"></script>
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

   可以通過為聲明查看器來設定其靜態大小 `.s7spinviewer` 頂級CSS類（以絕對單位表示），或使用 `stagesize` 修改量。

   可以將大小調整直接放在CSS中HTML頁或自定義查看器CSS檔案中。 稍後將其分配給Dynamic Media Classic的查看器預設記錄，或使用style命令顯式傳遞。

   請參閱 [自定義旋轉查看器](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-customizingviewer/c-html5-spin-viewer-customizingviewer.md#concept-464f3bfa55764bc09c92d8c7480b0b55) 的子菜單。

   以下是在「HTML」頁中定義靜態查看器大小的示例：

   ```html {.line-numbers}
   #s7viewer.s7spinviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   可以設定 `stagesize` 修改符，在Dynamic Media Classic的查看器預設記錄中。 或者，可以使用查看器初始化代碼顯式傳遞它， `params` 或作為API調用（如「命令參考」部分中所述），如下所示：

   ```html {.line-numbers}
    spinViewer.setParam("stagesize", 
   "640,480");
   ```

   建議使用基於CSS的方法，並在本示例中使用。

1. 建立和初始化查看器。

   完成上述步驟後，將建立 `s7viewers.SpinViewer` 類，將所有配置資訊傳遞給其建構子和調用 `init()` 的子常式。 配置資訊作為JSON對象傳遞給建構子。 至少，此對象 `containerId` 包含查看器容器ID和嵌套名稱的欄位 `params` JSON對象及其查看器支援的配置參數。 在本例中 `params` 對象，它至少必須將Image Serving URL作為 `serverUrl` 及初始資產 `asset` 的下界。 基於JSON的初始化API允許您使用單行代碼建立和啟動查看器。

   必須將查看器容器添加到DOM中，以便查看器代碼可以通過其ID查找容器元素。 某些瀏覽器將生成DOM延遲到網頁結束。 要獲得最大相容性，請調用 `init()` 方法 `BODY` 標籤，或者身上 `onload()` 的子菜單。

   同時，容器元素還不一定是網頁佈局的一部分。 例如，它可能是使用 `display:none` 指定的樣式。 在這種情況下，查看器將其初始化過程延遲到網頁將容器元素帶回佈局的那一刻。 當此操作發生時，查看器載入將自動恢復。

   以下是建立查看器實例的示例，將最小必要配置選項傳遞給建構子，並調用 `init()` 的雙曲餘切值。 該示例假定 `spinViewer` 是查看器實例， `s7viewer` 是佔位符的名稱 `DIV`。 [!DNL http://s7d1.scene7.com/is/image/] 是影像服務URL, [!DNL Scene7SharedAssets/SpinSet_Sample] 是資產。

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var spinViewer = new s7viewers.SpinViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/SpinSet_Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   以下代碼是嵌入固定大小的Spin Viewer的普通網頁的完整示例：

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7spinviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var spinViewer = new s7viewers.SpinViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/SpinSet_Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
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
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

以下示例頁說明了具有無限制高度的響應設計嵌入的更多實際使用案例：

[即時演示](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[備用演示位置](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**定義寬度和高度的柔性尺寸嵌入**

如果定義了寬度和高度的靈活大小嵌入，則網頁樣式會有所不同。 即，它為「保持器」提供兩種大小 `DIV` 並將其置於瀏覽器窗口中。 此外，網頁還設定 `HTML` 和 `BODY` 元素到100%:

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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
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
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7spinviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var spinViewer = new s7viewers.SpinViewer(); 
spinViewer.setContainerId("s7viewer"); 
spinViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
spinViewer.setAsset("Scene7SharedAssets/SpinSet_Sample"); 
spinViewer.init(); 
</script> 
</body> 
</html>
```
