---
description: 互動式視訊檢視器是播放以H.264格式編碼的串流和漸進式視訊的視訊播放器。
seo-description: 互動式視訊檢視器是播放以H.264格式編碼的串流和漸進式視訊的視訊播放器。
seo-title: 互動式視訊
solution: Experience Manager
title: 互動式視訊
topic: Dynamic media
uuid: 116c6b40-2490-4f1a-9c76-e06082069cc8
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# 互動式視訊{#interactive-video}

互動式視訊檢視器是播放以H.264格式編碼的串流和漸進式視訊的視訊播放器。

檢視器檢視器也會在視訊內容旁顯示互動式產品色票。 同時支援單一視訊和最適化視訊集。 它可在支援HTML5視訊的案頭和行動網頁瀏覽器上運作。 檢視器支援視訊內容上方顯示的選擇性隱藏字幕、視訊章節導覽和社交分享工具。 此檢視器的目的是協助您建置「可購買的視訊」體驗。 也就是說，使用者可以選取與特定視訊時區相關聯的色票，並重新導向至客戶網站上的快速檢視或產品詳細資訊頁面。

檢視器類型為510。

## 示範URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/glacier/InteractiveVideoViewerDemo.html](https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/glacier/InteractiveVideoViewerDemo.html)

和

[https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/AXIS/index.html](https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/AXIS/index.html)

## 系統要求 {#section-b7270cc4290043399681dc504f043609}

請參閱 [系統需求](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

## 使用互動式視訊檢視器 {#section-e6c68406ecdc4de781df182bbd8088b4}

互動式視訊檢視器代表主要JavaScript檔案和一組輔助檔案（單一JavaScript包含此特定檢視器、資產和CSS所使用的所有檢視器SDK元件），由檢視器在執行時期下載。

互動式視訊檢視器可在快顯模式下使用Image Serving檢視器隨附的可立即生產使用的HTML頁面。 它也可以在內嵌模式中使用，在此模式中，它會使用檔案化的API整合到目標網頁中。

設定和外觀設定與本指南中說明的其他檢視器類似。 所有外觀設定都是透過自訂(CSS)階層式樣式表來實現。

請參 [閱所有檢視器通用的命令參考——所有檢視器通用的組態屬性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)[和命令參考- URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 與互動式視訊檢視器互動 {#section-642e66ca38cd4032992840ec6c0b0cd2}

互動式視訊檢視器提供一組標準的視訊播放使用者介面控制項，例如播放／暫停按鈕、視訊筆畫、視訊時間泡泡、播放時間／總時間指示器、音量控制、全螢幕按鈕和隱藏字幕切換。 所有這些控制項都會直接在主檢視下方分組為控制列。

請注意，在觸控裝置上，音量控制會從使用者介面中隱藏，因為只有使用裝置的硬體按鈕才能控制音量。

當檢視器在快顯模式下運作時，使用者介面中就無法使用全螢幕按鈕。

檢視器會在視訊檢視區域右側顯示具有互動色票的面板。 當視訊播放時，色票清單會自動前進，以顯示與目前視訊區域對應的色票。 按一下或點選色票會觸發在作者期間與此色票關聯的動作。 視您的設定而定，觸發器可能會重新導向至網站上的不同頁面，或將產品資訊傳回網頁邏輯，而網頁邏輯則會觸發開啟顯示相關產品內容的快速檢視。

在啟動視訊旁白時，可快速導覽視訊內容。 視訊章節會在視訊筆畫軌道中顯示為標籤，並在滑鼠指向（或在觸控系統上按一下滑鼠）時顯示章節標題和說明。 客戶可以按一下章節標籤或點選章節描述泡泡，以「尋找」特定章節。

檢視器也支援各種社交媒體分享工具。 使用者介面中的單一按鈕可供使用，當使用者點選或點選時，此按鈕會展開為共用工具列。 共用工具列包含每種支援分享管道類型的圖示，例如Facebook、Twitter、電子郵件分享、內嵌代碼分享和連結分享。 當啟用電子郵件共用、內嵌共用或連結共用工具時，檢視器會顯示包含對應資料輸入表單的強制對話方塊。 呼叫Facebook或Twitter時，檢視器會將使用者從社交媒體服務重新導向至標準共用對話方塊。 此外，當共用工具啟動時，會自動暫停視訊播放。 由於網頁瀏覽器的安全性限制，共用工具無法在全螢幕模式下使用。

檢視器可完全透過鍵盤存取。 請參閱 [鍵盤協助功能和導覽](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 內嵌互動式視訊檢視器 {#section-6bb5d3c502544ad18a58eafe12a13435}

互動式視訊檢視器可內嵌至代管頁面。 這種網頁可以具有靜態版面，或者可以是「自適應」的，並在不同裝置上或不同瀏覽器視窗大小顯示不同。

為滿足這些需求，檢視器支援兩種主要作業模式：固定大小內嵌和回應式內嵌。

**關於固定大小嵌入模式和自適應設計嵌入模式**

在內嵌模式中，檢視器會新增至現有的網頁，而現有網頁可能已有與檢視器無關的客戶內容。 檢視器通常只佔用網頁的部分空間。

主要使用案例是針對桌上型電腦或平板電腦裝置的網頁，以及回應式設計的頁面，可根據裝置類型自動調整版面。

當檢視器在初始載入後未變更其大小時，會使用固定大小內嵌。 這是具有靜態版面的網頁的最佳選擇。

回應式設計內嵌假設檢視器可能需要在執行時期調整大小，以因應容器的大小變更 `DIV`。 最常見的使用案例是將檢視器新增至使用彈性頁面版面的網頁。

在回應式設計內嵌模式中，檢視器的運作方式視網頁大小容器而有所不同 `DIV`。 如果網頁只設定容器的寬度，而不限制其高度 `DIV`，檢視器會根據所使用資產的外觀比例自動選擇其高度。 此功能可確保資產完美整合至檢視中，而不會在側邊產生任何填補空間。 此使用案例是使用自適應網頁設計版面架構（例如引導、基礎等）的網頁最常見的使用案例。

否則，如果網頁同時設定檢視器容器的寬度和高度 `DIV`，檢視器會填滿該區域，並遵循網頁版面所提供的大小。 一個很好的例子是將檢視器內嵌至模態覆蓋，其中覆蓋會根據網頁瀏覽器視窗大小而調整大小。

**固定大小內嵌**

您可執行下列動作，將檢視器新增至網頁：

1. 將檢視器JavaScript檔案新增至您的網頁。
1. 定義容器 `DIV`。
1. 設定檢視器大小。
1. 建立和初始化檢視器。

1. 將檢視器JavaScript檔案新增至您的網頁。

   建立檢視器時，您必須在HTML標題中新增指令碼標籤。 在您使用檢視器API之前，請確定您已加入 [!DNL InterativeVideoViewer.js]。 此檔 [!DNL InteractiveVideoViewer.js] 案位於標準IS- [!DNL html5/js/] Viewer部署的子資料夾下：

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js]

如果檢視器部署在其中一個Adobe Dynamic Media Classic伺服器上，且是從相同網域提供，則可使用相對路徑。 否則，您會指定安裝IS-Viewer之一的Adobe Dynamic Media Classic伺服器的完整路徑。

相對路徑如下所示：

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>您只應參考頁面上的主要檢視 `include` 器JavaScript檔案。 您不應在網頁程式碼中參考檢視器邏輯在執行時期中可能下載的任何其他JavaScript檔案。 尤其是，請勿直接參考檢視器從內容路 `Utils.js` 徑載入的HTML5 SDK程 `/s7viewers` 式庫(稱為整合SDK `include`)。 原因是檢視器邏輯可完 `Utils.js` 全管理或類似執行時期檢視器程式庫的位置，而檢視器版本之間的位置也會改變。 Adobe不會在伺服器上保留舊版次 `includes` 要檢視器。
>
>
>因此，將檢視器使用的任何次要JavaScript `include` 直接參考放在頁面上，將來部署新產品版本時，檢視器功能會中斷。

1. 定義容器 `DIV`。

   將空白元 `DIV` 素新增至您要檢視器出現的頁面。 元 `DIV` 素必須已定義其ID，因為此ID稍後會傳遞至檢視器API。 DIV的大小是透過CSS指定的。

   預留位 `DIV` 置是定位的元素，表示 `position` CSS屬性已設為 `relative` 或 `absolute`。

   若要讓全螢幕功能在Internet Explorer中正常運作，請確定DOM中沒有其他元素的堆疊順序高於預留位置 `DIV`。

   以下是已定義預留位置元素的范 `DIV` 例：

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. 設定檢視器大小

   您可以設定檢視器的靜態大小，方法是以絕對單位 `.s7interactivevideoviewer` 來宣告頂層CSS類別，或使用修飾 `stagesize` 元。

   您可以直接將大小調整置於CSS中的HTML頁面，或自訂檢視器CSS檔案中，這些檔案稍後會指派給AEM Assets中的檢視器預設記錄——隨選，或使用命令明確傳遞 `style` 。

   如需 [使用CSS設定檢視器樣式的詳細資訊，請參閱自訂互動式視訊檢視器](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) 。

   以下是在HTML頁面中定義靜態檢視器大小的範例：

   ```
   #s7viewer.s7interactivevideoviewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   您可以在AEM Assets - `stagesize` on-demand的檢視器預設記錄中設定修飾元。 或者，您可將它與檢視器初始化程式碼搭配使用 `params` collection明確傳遞，或以API呼叫的方式傳遞，如下所示：

   ```
   interactivevideoviewer.setParam("stagesize", "640,640");
   ```

   建議使用以CSS為基礎的方法，並在此範例中使用。

1. 建立和初始化檢視器。

   完成上述步驟後，您將建立類的實例、將所有配置資訊傳遞給其建構子 `s7viewers.InteractiveVideoViewer` ，並在查看器實例 `init()` 上調用方法。 設定資訊會以JSON物件的形式傳遞至建構函式。 至少，此物件應具有欄 `containerId` 位，其中包含檢視器容器ID的名稱，以及檢視器支援的組態參數巢狀 `params` JSON物件。

   在此情況下，物 `params` 件必須至少將「影像伺服URL」傳遞為屬 `serverUrl` 性，並將初始資產傳遞為 `asset` 參數。 以JSON為基礎的初始化API可讓您使用單一程式碼行、視訊伺服器URL作為屬性傳遞、初始資產作為參數，以及互動資料作為屬性來建立和啟動檢 `videoserverurl``asset``interactivedata` 視器。 以JSON為基礎的初始化API可讓您使用單行程式碼來建立和啟動檢視器。

   請務必將檢視器容器新增至DOM，如此檢視器程式碼就能依其ID找到容器元素。 有些瀏覽器會延遲建立DOM，直到網頁結束為止。 為獲得最大相容性，請 `init()` 在結束標籤之前或在 `BODY` body事件上呼叫方 `onload()` 法。

   同時，容器元素也不一定是網頁版面的一部分。 例如，它可能會使用指派給它 `display:none` 的樣式隱藏。 在此情況下，檢視器會延遲其初始化程式，直到網頁將容器元素帶回版面為止。 此時，檢視器載入會自動繼續。

   以下是建立檢視器例項的範例，將最小必要的設定選項傳遞至建構函式並呼叫 `init()` 方法。 該示例假設如下：

   * 檢視器例項為 `interactiveVideoViewer`。
   * 佔位符的名 `DIV` 稱為 `s7viewer`。
   * 影像伺服URL為 `https://aodmarketingna.assetsadobe.com/is/image/`。
   * 視訊伺服器URL為 `https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna`。
   * 內容URL為 `https://aodmarketingna.assetsadobe.com/`。
   * 資產是 `/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4`。
   * 互動式資料就是 `is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt`。

   ```
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

   以下程式碼是內嵌固定大小之互動式視訊檢視器之簡單網頁的完整範例：

   ```
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

**不受高度限制的自適應設計內嵌**

有了互動式設計內嵌功能，網頁通常就有某種靈活的版面配置，可決定檢視器容器的執行時期大小 `DIV`。 在下列範例中，假設網頁允許檢視器的容器取用40%的 `DIV` 網頁瀏覽器視窗大小，而不會限制其高度。 網頁HTML程式碼如下所示：

```
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

將檢視器新增至此類頁面的步驟類似於固定大小內嵌的步驟。 唯一的區別是您不需要明確定義檢視器大小。

1. 將檢視器JavaScript檔案新增至您的網頁。
1. 定義容器DIV。
1. 建立和初始化檢視器。

上述所有步驟都與固定大小內嵌相同。 將容器DIV新增至現有 `"holder"` DIV。 以下程式碼為完整範例。 請注意，當重新調整瀏覽器大小時，檢視器大小會變更，以及檢視器外觀比例如何符合資產。

```
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

下列範例頁面說明在實際使用中，不受高度限制的互動式設計內嵌功能：

[https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html](https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html)

**定義寬度和高度的自適應內嵌**

如果定義了寬度和高度的互動式內嵌，網頁樣式會有所不同。 它為DIV提供兩種大小， `"holder"` 並將其置於瀏覽器視窗中。 此外，網頁會將元素和元素的大 `HTML` 小設 `BODY` 為100%。

```
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

其餘的嵌入步驟與不受限高度的自適應嵌入步驟相同。 產生的範例如下：

```
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

**使用Setter型API內嵌**

您可以使用setter-based API和no-args建構函式，而不是使用JSON型初始化。 使用此API建構函式時，不會使用任何參數，而設定參數是使用 `setContainerId()`、 `setParam()``setAsset()` API方法以及個別的JavaScript呼叫來指定。

下列範例說明如何搭配基於setter的API使用固定大小內嵌：

```
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

