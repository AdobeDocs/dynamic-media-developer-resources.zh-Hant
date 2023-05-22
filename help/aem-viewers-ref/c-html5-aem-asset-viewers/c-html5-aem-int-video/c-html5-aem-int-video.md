---
title: 互動式視頻
description: 互動式視頻查看器是播放以H.264格式編碼的流式和漸進式視頻的視頻播放器。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: e54b0b1f-b015-4592-82e2-99f5080543e3
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2211'
ht-degree: 0%

---

# 互動式視頻{#interactive-video}

互動式視頻查看器是播放以H.264格式編碼的流式和漸進式視頻的視頻播放器。

查看器還顯示視頻內容旁邊的互動式產品色板。 同時支援單個視頻和自適應視頻集。 它設計用於支援HTML5視頻的案頭和移動Web瀏覽器。 觀看者支援在視頻內容、視頻章節導航和社交共用工具頂部顯示的可選隱藏字幕。 此查看器的目的是幫助您實現「可購買視頻」體驗。 即，用戶可以選擇與特定視頻時間區域關聯的色板，然後重定向到客戶網站上的Quickview或產品詳細資訊頁面。

查看器類型為510。

## 演示URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/glacier/InteractiveVideoViewerDemo.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/glacier/InteractiveVideoViewerDemo.html)

和

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/AXIS/index.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/AXIS/index.html)

## 系統要求 {#section-b7270cc4290043399681dc504f043609}

請參閱 [系統要求](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

## 使用互動式視頻查看器 {#section-e6c68406ecdc4de781df182bbd8088b4}

互動式視頻查看器表示主JavaScript檔案和查看器在運行時下載的幫助檔案集。 此特定查看器、資產和CSS使用的所有Viewer SDK元件都包含一個JavaScript。

互動式視頻查看器可以使用隨影像服務查看器提供的生產就緒HTML頁在彈出模式下使用。 它還可以在嵌入式模式下使用，在該模式下，它使用文檔化的API被整合到目標網頁中。

配置和外觀與本指南中介紹的其他查看器的配置和外觀相似。 所有蒙皮都通過自定義(CSS)層疊樣式表實現。

請參閱 [所有查看器通用的命令引用 — 配置屬性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 和 [所有查看器通用的命令引用 — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 與互動式視頻查看器交互 {#section-642e66ca38cd4032992840ec6c0b0cd2}

互動式視頻查看器提供一組用於視頻播放的標準用戶介面控制項，如播放/暫停按鈕、視頻掃描器、視頻時間氣泡、播放時間/總時間指示器、音量控制、全屏按鈕和關閉字幕切換。 所有這些控制項都直接在主視圖下被分組到控制欄中。

在觸摸設備上，卷控制項被隱藏在用戶介面之外，因為只能使用設備的硬體按鈕來控制卷。

當查看器在彈出模式下操作時，用戶介面中不提供全屏按鈕。

查看器顯示一個面板，其中帶有視頻查看區域右側的互動式色板。 當視頻播放時，色板清單會自動進行前移，以便顯示與當前視頻區域對應的色板。 按一下或點擊某個色板會觸發在創作期間與此類色板關聯的操作。 根據您的設定方式，觸發器可能會重定向到網站上的其他頁面。 或者，它可以將產品資訊傳回網頁邏輯，而網頁邏輯又可以觸發顯示相關產品內容的Quickview的開啟。

當視頻章節被激活時，可以快速瀏覽視頻內容。 視頻章節在視頻掃描器跟蹤中顯示為標籤，並在滾動時（或在觸摸系統上按一下時）顯示章節標題和說明。 客戶可以通過按一下章節標籤或點擊章節描述氣泡來「查找」特定章節。

觀眾還支援各種社交媒體共用工具。 它們可作為用戶介面中的單個按鈕使用，當用戶按一下或輕擊該按鈕時，該按鈕會擴展到共用工具欄。 共用工具欄包含支援的每種類型的共用通道的表徵圖，如Facebook、Twitter、電子郵件共用、嵌入代碼共用和連結共用。 當激活電子郵件共用、嵌入共用或連結共用工具時，查看器將顯示帶有相應資料輸入表單的模式對話框。 當呼叫Facebook或Twitter時，觀看者將用戶從社交媒體服務重定向到標準共用對話框。 此外，當共用工具被激活時，視頻回放將自動暫停。 由於Web瀏覽器安全限制，共用工具在全屏模式下不可用。

可以完全使用鍵盤訪問查看器。 請參閱 [鍵盤輔助功能和導航](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 嵌入互動式視頻查看器 {#section-6bb5d3c502544ad18a58eafe12a13435}

互動式視頻查看器嵌入到宿首頁面中。 這種網頁可具有靜態佈局，或者它可以「響應」，並在不同設備上或不同瀏覽器窗口大小上顯示不同。

為滿足這些需要，查看器支援兩種主要操作模式：固定大小嵌入和響應嵌入。

**關於固定尺寸嵌入模式和響應設計嵌入模式**

在嵌入模式中，查看器被添加到現有網頁中，該網頁可能已經具有與查看器無關的一些客戶內容。 瀏覽者通常只佔用網頁的一部分房地產。

主要使用案例是面向台式機或平板電腦設備的網頁，以及響應性設計的頁面，這些頁面根據設備類型自動調整佈局。

當查看器在初始載入後不更改其大小時，使用固定大小嵌入。 此功能是具有靜態佈局的網頁的最佳選擇。

響應性設計嵌入假定查看器需要在運行時調整大小以響應其容器的大小變化 `DIV`。 最常見的用例是向使用靈活頁面佈局的網頁添加查看器。

在響應性設計嵌入模式中，查看器根據網頁大小其容器的方式而具有不同的行為 `DIV`。 如果網頁僅設定容器的寬度 `DIV`在保持高度不受限制的情況下，觀看者根據所使用資產的縱橫比自動選擇其高度。 此功能可確保資產完美地貼入視圖中，而不會在側面出現任何填充。 此使用案例是使用響應性Web設計佈局框架(如Bootstrap和Foundation)的Web頁面中最常見的使用案例。

否則，如果網頁為查看者的容器設定寬度和高度 `DIV`，查看器僅填充該區域並遵循網頁佈局提供的大小。 一個很好的例子是將查看器嵌入到模式覆蓋中，其中覆蓋根據Web瀏覽器窗口大小進行大小調整。

**固定大小嵌入**

通過執行以下操作，可將查看器添加到網頁：

1. 將查看器JavaScript檔案添加到網頁。
1. 定義容器 `DIV`。
1. 設定查看器大小。
1. 建立和初始化查看器。

1. 將查看器JavaScript檔案添加到網頁。

   建立查看器要求在HTML頭中添加指令碼標籤。 在使用查看器API之前，請確保包括 [!DNL InterativeVideoViewer.js]。 的 [!DNL InteractiveVideoViewer.js] 檔案位於 [!DNL html5/js/] 標準IS查看器部署的子資料夾：

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js]

如果查看器部署在其中一個Adobe Dynamic Media Classic伺服器上，並且從同一域提供服務，則可以使用相對路徑。 否則，您將指定到安裝了IS-Viewers的Adobe Dynamic Media Classic伺服器之一的完整路徑。

相對路徑如下所示：

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>僅引用主查看器JavaScript `include` 檔案。 不要引用網頁代碼中任何可能在運行時由查看器邏輯下載的附加JavaScript檔案。 特別是，不直接引用HTML5 SDK `Utils.js` 由查看器從 `/s7viewers` 上下文路徑（所謂統一SDK） `include`)。 原因是 `Utils.js` 或類似的運行時查看器庫由查看器的邏輯和查看器版本之間的位置更改進行完全管理。 Adobe不保留舊版次查看器 `includes` 在伺服器上。
>
>
>因此，直接引用任何輔助JavaScript `include` 該頁面上的查看器使用的瀏覽器功能將在部署新產品版本時中斷查看器功能。

1. 定義容器 `DIV`。

   添加空 `DIV` 元素。 的 `DIV` 元素必須定義其ID，因為此ID稍後會傳遞給查看器API。 DIV的大小通過CSS指定。

   佔位符 `DIV` 是定位元素，表示 `position` CSS屬性設定為 `relative` 或 `absolute`。

   要使全屏功能在Internet Explorer中正常工作，請確保DOM中沒有其他元素的堆疊順序高於佔位符 `DIV`。

   以下是定義佔位符的示例 `DIV` 元素：

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. 設定查看器大小

   可以通過為聲明查看器來設定其靜態大小 `.s7interactivevideoviewer` 頂級CSS類（以絕對單位表示），或使用 `stagesize` 修改量。

   您可以將大小調整直接放在CSS中的HTML頁。 或者，可以將其放入自定義查看器CSS檔案中，該檔案稍後將分配給Adobe Experience Manager資產 — 按需分配的查看器預設記錄，或使用顯式傳遞 `style` 的子菜單。

   請參閱 [自定義互動式視頻查看器](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) 的子菜單。

   下面是在HTML頁中定義靜態查看器大小的示例：

   ```html {.line-numbers}
   #s7viewer.s7interactivevideoviewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   可以設定 `stagesize` 在Experience Manager Assets的查看器預設記錄中的修飾符 — 按需。 或者，可以使用查看器初始化代碼顯式傳遞它， `params` 或作為「命令引用」部分中所述的API調用，如下所示：

   ```html {.line-numbers}
   interactivevideoviewer.setParam("stagesize", "640,640");
   ```

   建議使用基於CSS的方法，並在本示例中使用。

1. 建立和初始化查看器。

   完成上述步驟後，將建立 `s7viewers.InteractiveVideoViewer` 類，將所有配置資訊傳遞給其建構子，並調用 `init()` 的子常式。 配置資訊作為JSON對象傳遞給建構子。 至少，此對象應 `containerId` 包含查看器容器ID名稱和嵌套的欄位 `params` 具有查看器支援的配置參數的JSON對象。

   在這個例子中， `params` 對象必須至少將Image Serving URL傳遞為 `serverUrl` 及初始資產 `asset` 的下界。 通過基於JSON的初始化API，您可以建立並啟動查看器，並使用一行代碼、傳遞為 `videoserverurl` 物業、初始資產 `asset` 參數和交互資料 `interactivedata` 屬性。 基於JSON的初始化API允許您使用單行代碼建立和啟動查看器。

   必須將查看器容器添加到DOM中，以便查看器代碼可以通過其ID查找容器元素。 某些瀏覽器將生成DOM延遲到網頁結束。 要獲得最大相容性，請調用 `init()` 方法 `BODY` 標籤，或者身上 `onload()` 的子菜單。

   同時，容器元素還不一定是網頁佈局的一部分。 例如，它可能隱藏在 `display:none` 指定的樣式。 在這種情況下，查看器將其初始化過程延遲到網頁將容器元素帶回佈局的那一刻。 發生這種情況時，查看器載入將自動恢復。

   以下是建立查看器實例的示例，將最小必要配置選項傳遞給建構子，並調用 `init()` 的雙曲餘切值。 該示例假定：

   * 查看器實例為 `interactiveVideoViewer`。
   * 佔位符的名稱 `DIV` 是 `s7viewer`。
   * 影像服務URL為 `https://aodmarketingna.assetsadobe.com/is/image/`。
   * 視頻伺服器URL為 `https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna`。
   * 內容URL為 `https://aodmarketingna.assetsadobe.com/`。
   * 資產 `/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4`。
   * 交互資料是 `is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt`。

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
   "config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
    "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
    "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
    "contenturl":"https://aodmarketingna.assetsadobe.com/", 
   "interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
   } 
   }).init(); 
   </script>
   ```

   以下代碼是嵌入固定大小的互動式視頻查看器的簡單網頁的完整示例：

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7interactivevideoviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;"></div> 
   <script type="text/javascript"> 
   var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
   "config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
    "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
    "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
    "contenturl":"https://aodmarketingna.assetsadobe.com/", 
   "interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**具有無限制高度的響應設計嵌入**

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
<script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
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
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
"config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
 "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
 "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
 "contenturl":"https://aodmarketingna.assetsadobe.com/", 
"interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
} 
}).init(); 
</script> 
</body> 
</html>
```

以下示例頁說明了具有無限制高度的響應設計嵌入在現實生活中的更多用途：

[即時演示](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[備用演示位置](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**定義寬度和高度的響應嵌入**

如果定義了寬度和高度的響應嵌入，則網頁樣式是不同的。 它為 `"holder"` DIV並將其置於瀏覽器窗口中。 此外，網頁還設定 `HTML` 和 `BODY` 元素到100%。

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

其餘的嵌入步驟與用於具有無限制高度的響應嵌入的步驟相同。 結果示例如下：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
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
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
"config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
 "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
 "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
 "contenturl":"https://aodmarketingna.assetsadobe.com/", 
"interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**使用基於Setter的API嵌入**

可以不使用基於JSON的初始化，而是使用基於setter的API和no-args建構子。 使用此API建構子不採用任何參數，配置參數是使用 `setContainerId()`。 `setParam()`, `setAsset()` API方法，具有單獨的JavaScript調用。

以下示例說明了將固定大小嵌入與基於setter的API一起使用：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7interactivevideoviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer(); 
interactiveVideoViewer.setContainerId("s7viewer"); 
interactiveVideoViewer.setParam("config", "/etc/dam/presets/viewer/Shoppable_Video_Dark"); 
interactiveVideoViewer.setParam("serverurl", "https://aodmarketingna.assetsadobe.com/is/image/"); 
interactiveVideoViewer.setParam("videoserverurl", "https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna"); 
interactiveVideoViewer.setParam("contenturl", "https://aodmarketingna.assetsadobe.com/"); 
interactiveVideoViewer.setParam("interactivedata", "is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt"); 
interactiveVideoViewer.setAsset("/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4"); 
interactiveVideoViewer.init(); 
</script> 
</body> 
</html>
```
