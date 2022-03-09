---
title: 智慧裁剪視頻查看器
description: Smart Crop視頻查看器是一個視頻播放器，在添加智慧裁剪支援的同時播放以H.264格式編碼的流和漸進式視頻。 它是從Dynamic Media Classic或Adobe Experience Manager和Dynamic Media運送的。
keywords: 響應
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 937be8a2-307e-47bb-9fc8-d354f780a214
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2413'
ht-degree: 0%

---

# 智慧裁剪視頻{#smart-crop-video}

Smart Crop視頻查看器是一個視頻播放器，在添加智慧裁剪支援的同時播放以H.264格式編碼的流和漸進式視頻。 它是從Dynamic Media Classic或與Dynamic MediaExperience Manager運送的。

請參閱 [系統要求和先決條件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

同時支援單個視頻和自適應視頻集。 此外，查看器支援使用外部位置上承載的漸進式視頻和HLS流。 它設計用於支援HTML5視頻的案頭和移動Web瀏覽器。 此查看器還支援視頻內容、視頻章節導航和社交媒體共用工具頂部顯示的可選隱藏字幕。

Smart Crop Video Viewer在基礎系統支援時使用HLS格式的HTML5流視頻回放，其預設配置為。 在不支援HTML5流式傳輸的系統上，查看器將返回HTML5逐步視頻傳輸。

查看器類型518。

## 演示URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS](https://s7d9.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS)

## 使用Smart Crop Video Viewer {#section-f21ac23d3f6449ad9765588d69584772}

Smart Crop Video Viewer表示主JavaScript檔案和一組幫助檔案 — 單個JavaScript包含該查看器在運行時下載的所有查看器SDK元件、資產和CSS。

您可以使用隨IS-Viewers提供的生產就緒HTML頁，在彈出模式下使用Smart Crop視頻查看器。 或者，您可以在嵌入式模式下使用查看器，在該模式下，使用文檔化的API將查看器整合到目標網頁中。

配置和設定查看器外觀的任務與其他查看器類似。 所有蒙皮都是通過自定義CSS實現的。

請參閱 [所有查看器通用的命令引用 — 配置屬性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 和 [所有查看器通用的命令引用 — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 與Smart Crop Video Viewer交互 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Smart Crop Video Viewer為視頻播放提供一組標準用戶介面控制項，例如：

* 「播放/暫停」按鈕。
* 視頻掃描器視頻時間氣泡。
* 播放時間/總時間指示器。
* 音量控制。
* 全屏按鈕。
* 隱藏字幕切換。

所有這些控制項都分組到查看器用戶介面底部的控制欄中。

在觸摸設備上，音量控制隱藏在用戶介面之外，因為只能使用硬體按鈕來控制音量。

當查看器在彈出模式下操作時，用戶介面中不提供全屏按鈕。

當視頻章節被激活時，可以快速瀏覽視頻內容。 視頻章節在視頻掃描器軌道中顯示為標籤，並在滑鼠翻轉或在觸摸系統上按一下時顯示章節標題和相關說明。 用戶可以通過選擇章節標籤或選擇章節說明氣泡來查找特定章節。

該查看器支援Windows設備上的觸摸輸入和滑鼠輸入，並帶有觸摸屏和滑鼠。 但是，此支援僅限於Chrome、Internet Explorer 11和Edge Web瀏覽器。

此查看器可完全以鍵盤方式訪問。

請參閱 [鍵盤輔助功能和導航](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 使用Smart Crop Video Viewer的社交媒體共用工具 {#section-907d316fe1da4b87abb9775f02464704}

Smart Crop視頻查看器支援社交媒體共用工具。 它們可作為用戶介面中的單個按鈕使用，當用戶按一下或輕擊該按鈕時，該按鈕會擴展到共用工具欄。

共用工具欄包含支援的每種類型共用通道的表徵圖，如Facebook、Twitter、電子郵件共用、嵌入代碼共用和連結共用。 當激活電子郵件共用、嵌入共用或連結共用工具時，查看器將顯示帶有相應資料輸入表單的模式對話框。 當呼叫Facebook或Twitter時，觀看者將用戶從社交媒體服務重定向到標準共用對話框。 同樣，當共用工具被激活時，視頻回放會自動暫停。

由於Web瀏覽器安全限制，共用工具在全屏模式下不可用。

## 嵌入Smart Crop視頻查看器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同的網頁對查看者行為有不同的需求。 有時，網頁提供的連結在選中時會在單獨的瀏覽器窗口中開啟查看器。 在其他情況下，必須將查看器直接嵌入到托管頁面中。 在後一種情況下，該網頁可以具有靜態頁面佈局，或者使用響應設計，該響應設計在不同的設備上顯示不同的或針對不同的瀏覽器窗口大小。 為滿足這些需要，查看器支援三種主要操作模式：彈出式、固定大小嵌入和響應性設計嵌入。

平板電腦和移動設備支援在同一頁面上嵌入多個視頻。 通常，一次只能播放一個視頻。 當用戶開始播放一個視頻，然後嘗試播放另一個視頻時，第一個視頻將自動暫停。 自動暫停的視頻會記住其當前的播放時間，因此用戶可以始終返回到它並繼續播放。 此規則唯一的例外是Android™ 4.x設備上的Chrome瀏覽器，該瀏覽器可以並行播放視頻。

**關於彈出模式**

在彈出模式下，在單獨的Web瀏覽器窗口或頁籤中開啟查看器。 它會佔用整個瀏覽器窗口區域，並在瀏覽器調整大小或設備方向發生變化時進行調整。

此模式是移動設備中最常見的模式。 網頁使用 `window.open()` JavaScript調用，正確配置 `A` HTML元件或任何其它合適的方法。

建議您使用現成HTML頁面進行彈出操作模式。 它叫 [!DNL SmartCropVideoViewer.html] 它位於 [!DNL html5/] 標準IS查看器部署的子資料夾：

[!DNL <s7viewers_root>/html5/SmartCropVideoViewer.html]

通過應用自定義CSS，可以實現可視化定製。

以下是在新窗口中開啟查看器的HTML代碼示例：

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS" target="_blank">Open popup viewer</a>
```

**關於固定尺寸嵌入模式和響應嵌入模式**

在嵌入模式中，查看器被添加到現有網頁中，該網頁可能已經具有與查看器無關的一些客戶內容。 瀏覽者通常只佔據網頁的一部分房地產。

主要使用案例是面向台式機或平板電腦設備的網頁，還有響應性設計頁面，根據設備類型自動調整佈局。

在初始載入後查看器不更改其大小時，使用固定大小嵌入。 此選項是具有靜態頁面佈局的網頁的最佳選項。

響應性設計嵌入假定查看器必須在運行時調整大小以響應其容器的大小變化 `DIV`。 最常見的用例是將查看器添加到使用靈活頁面佈局的網頁。

在響應性設計嵌入模式中，查看器根據網頁大小其容器的方式而具有不同的行為 `DIV`。 如果網頁僅設定容器的寬度 `DIV`在保持高度不受限制的情況下，觀看者根據所使用資產的縱橫比自動選擇其高度。 該方法確保資產完全適合於視圖，而不會在側面出現任何填充。 對於使用響應性設計佈局框架(如Bootstrap或基礎)的網頁，此使用案例最常見。

否則，如果網頁為查看者的容器設定寬度和高度 `DIV`，查看器僅填充該區域並遵循網頁佈局提供的大小。 一個很好的例子是將查看器嵌入到模式覆蓋中，其中覆蓋根據Web瀏覽器窗口的大小進行大小調整。

**固定大小嵌入**

通過執行以下操作，可將查看器添加到網頁：

1. 將查看器JavaScript檔案添加到網頁。
1. 定義容器 `DIV`。
1. 設定查看器大小。
1. 建立和初始化查看器。

1. 將查看器JavaScript檔案添加到網頁。

   建立查看器要求在HTML頭中添加指令碼標籤。 在使用查看器API之前，請確保包括 [!DNL SmartCropVideoViewer.js]。 的 [!DNL SmartCropVideoViewer.js] 檔案位於 [!DNL html5/js/] 標準IS查看器部署的子資料夾：

[!DNL <s7viewers_root>/html5/js/SmartCropVideoViewer.js]

如果查看器部署在其中一個Adobe Dynamic Media Classic伺服器上，並且從同一域提供服務，則可以使用相對路徑。 否則，您將指定到安裝了IS-Viewers的Adobe Dynamic Media Classic伺服器之一的完整路徑。

相對路徑如下所示：

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/SmartCropVideoViewer.js"></script>
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

   確保全屏功能在Internet Explorer中正常工作。 檢查以確保DOM中沒有堆疊順序高於佔位符DIV的其他元素。

   以下是定義的佔位符DIV元素的示例：

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. 設定查看器大小

   可以通過為聲明查看器來設定其靜態大小 `.s7videoviewer` 頂級CSS類（以絕對單位表示），或使用修飾符 `stagesize`。

   您可以將大小設定在HTML頁的CSS中，或在自定義查看器CSS檔案中。 稍後將其分配給Dynamic Media Classic的查看器預設記錄，或使用style命令顯式傳遞。

   請參閱 [自定義智慧裁剪視頻查看器](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e) 的子菜單。

   以下是在HTML頁中定義靜態查看器大小的示例：

   ```html {.line-numbers}
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   可以設定 `stagesize` 修飾符，在Dynamic Media Classic的查看器預設記錄中，或用查看器初始化代碼將其顯式傳遞 `params` 的下界。 或者，如「命令參考」部分所述，作為API調用，如下所述：

   ```html {.line-numbers}
   smartCropVideoViewer.setParam("stagesize", "640,480");
   ```

   建議使用基於CSS的方法，並在本示例中使用。

1. 建立和初始化查看器。

   完成上述步驟後，將建立 `s7viewers.SmartCropVideoViewer` 類，將所有配置資訊傳遞給其建構子，並調用 `init()` 的子常式。 配置資訊作為JSON對象傳遞給建構子。 至少，此對象應 `containerId` 包含查看器容器ID和嵌套名稱的欄位 `params` 具有查看器支援的配置參數的JSON對象。 在這個例子中， `params` 對象必須至少將Image Serving URL傳遞為 `serverUrl` 屬性，視頻伺服器URL傳遞為 `videoserverurl` 及初始資產 `asset` 的下界。 基於JSON的初始化API允許您使用單行代碼建立和啟動查看器。

   必須將查看器容器添加到DOM中，以便查看器代碼可以通過其ID查找容器元素。 某些瀏覽器將生成DOM延遲到網頁結束。 要獲得最大相容性，請調用 `init()` 方法 `BODY` 標籤，或者身上 `onload()` 的子菜單。

   同時，容器元素還不一定是網頁佈局的一部分。 例如，它可能隱藏在 `display:none` 指定的樣式。 在這種情況下，查看器將其初始化過程延遲到網頁將容器元素帶回佈局的那一刻。 當此操作發生時，查看器載入將自動恢復。

   以下是建立查看器實例、將最小必要配置選項傳遞給建構子並調用 `init()` 的雙曲餘切值。 此示例假定 `smartCropVideoViewer` 是查看器實例， `s7viewer` 是佔位符的名稱 `DIV`。 [!DNL http://s7d1.scene7.com/is/image/] 是影像服務URL, [!DNL http://s7d1.scene7.com/is/content/] 是視頻伺服器URL, [!DNL html5automation/frisbee-AVS] 是資產。

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"html5automation/frisbee-AVS", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   ```

   以下代碼是嵌入Smart Crop視頻查看器且大小固定的普通網頁的完整示例：

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   <script type="text/javascript"> 
   var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"html5automation/frisbee-AVS", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html> 
   ```

**具有無限制高度的響應設計嵌入**

通過響應性設計嵌入，網頁通常具有某種靈活的佈局，其指示觀看者容器的運行時大小 `DIV`。 在本示例中，假定網頁允許查看者的容器 `DIV` 以取Web瀏覽器窗口大小的40%，使其高度不受限制。 網頁HTML代碼如下所示：

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

將查看器添加到此頁麵類似於固定大小嵌入；唯一的區別是您不需要顯式定義查看器大小。

1. 將查看器JavaScript檔案添加到網頁。
1. 定義容器DIV。
1. 建立和初始化查看器。

上述步驟與固定尺寸嵌入步驟相同。 添加容器 `DIV` 持有人」 `DIV`。 以下代碼是一個完整的示例。 您可以看到在調整瀏覽器大小時查看器大小的變化，以及查看器縱橫比與資產的匹配情況。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
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
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"html5automation/frisbee-AVS", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
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

其餘的嵌入步驟與具有無限制高度的響應設計嵌入相同。 結果示例如下：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
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
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"html5automation/frisbee-AVS", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7videoviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer(); 
smartCropVideoViewer.setContainerId("s7viewer"); 
smartCropVideoViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
smartCropVideoViewer.setParam("videoserverurl", "http://s7d1.scene7.com/is/content/"); 
smartCropVideoViewer.setAsset("html5automation/frisbee-AVS"); 
smartCropVideoViewer.init(); 
</script> 
</body> 
</html> 
```
