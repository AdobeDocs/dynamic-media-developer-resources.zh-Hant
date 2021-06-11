---
description: 互動式視訊檢視器是視訊播放器，會播放以H.264格式編碼的串流和漸進式視訊。
solution: Experience Manager
title: 互動式影片
feature: Dynamic Media Classic，檢視器， SDK/API，互動式影片
role: Developer,Business Practitioner
exl-id: e54b0b1f-b015-4592-82e2-99f5080543e3
source-git-commit: 6df782b389f7e14b8ad510ebb6f143ece0db23c9
workflow-type: tm+mt
source-wordcount: '2221'
ht-degree: 0%

---

# 互動式視訊{#interactive-video}

互動式視訊檢視器是視訊播放器，會播放以H.264格式編碼的串流和漸進式視訊。

檢視器也會顯示視訊內容旁的互動式產品色票。 支援單一視訊和最適化視訊集。 它專為支援HTML5視訊的案頭和行動網頁瀏覽器所設計。 檢視器支援視訊內容、視訊章節導覽和社交分享工具頂端顯示的選用隱藏式字幕。 此檢視器的用途是協助您實作「可購買的視訊」體驗。 也就是說，使用者可以選取與特定視訊時區相關聯的色票，然後重新導向至客戶網站上的快速檢視或產品詳細資訊頁面。

檢視器類型為510。

## 示範URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/glacier/InteractiveVideoViewerDemo.html](https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/glacier/InteractiveVideoViewerDemo.html)

及

[https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/AXIS/index.html](https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/AXIS/index.html)

## 系統要求 {#section-b7270cc4290043399681dc504f043609}

請參閱[系統要求](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

## 使用互動式視訊檢視器{#section-e6c68406ecdc4de781df182bbd8088b4}

互動式視訊檢視器代表主要JavaScript檔案，以及檢視器在執行階段下載的一組協助檔案。 此特定檢視器、資產和CSS使用的所有檢視器SDK元件皆包含單一JavaScript。

互動式視訊檢視器可在快顯模式中使用，使用隨附影像伺服檢視器的可生產用HTML頁面。 它也可在內嵌模式中使用，透過記錄的API整合至目標網頁。

設定和外觀與本指南中所述其他檢視器的設定和外觀類似。 所有外觀設定都是透過自訂(CSS)階層式樣式表來達成。

請參閱所有檢視器通用的[命令參考 — 設定屬性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)和所有檢視器通用的[命令參考 — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 與互動式視訊檢視器互動{#section-642e66ca38cd4032992840ec6c0b0cd2}

互動式視訊檢視器提供一組用於視訊播放的標準使用者介面控制項，例如播放/暫停按鈕、視訊清除器、視訊時間泡泡、播放時間/總時間指標、音量控制、全螢幕按鈕和隱藏式字幕切換。 所有這些控制項都會直接歸類到主檢視下的控制列中。

在觸摸設備上，音量控制在用戶介面中隱藏，因為只能使用設備的硬體按鈕控制音量。

檢視器在快顯模式中運作時，使用者介面中無法使用全螢幕按鈕。

檢視器會在視訊檢視區域的右側顯示具有互動色票的面板。 色票清單會在播放視訊時自動前進，以顯示與目前視訊區域對應的色票。 按一下或點選色票會觸發在製作期間與此色票相關聯的動作。 根據您的設定方式，觸發器可能會重新導向至網站上的不同頁面。 或者，它會將產品資訊傳回網頁邏輯，而邏輯又會觸發顯示相關產品內容的快速檢視的開啟。

啟動視訊分段時，可快速導覽視訊內容。 視訊章節會在視訊清除程式追蹤中顯示為標籤，並在滑鼠經過時（或在觸控式系統上按一下滑鼠即可）顯示章節標題和說明。 客戶可以按一下章節標籤或點選章節說明泡泡，以「搜尋」特定章節。

檢視器也支援各種社交媒體分享工具。 使用者按一下或點選使用者介面中的單一按鈕，即可展開至共用工具列。 共用工具列包含支援之每種共用管道類型的圖示，例如Facebook、Twitter、電子郵件共用、內嵌程式碼共用和連結共用。 啟用電子郵件共用、內嵌共用或連結共用工具時，檢視器會顯示含有對應資料輸入表單的強制回應對話方塊。 呼叫Facebook或Twitter時，檢視器會將使用者重新導向至社交媒體服務的標準共用對話方塊。 此外，共用工具啟動時，視訊播放會自動暫停。 由於網頁瀏覽器安全性限制，無法以全螢幕模式使用共用工具。

檢視器可完全鍵盤存取。 請參閱[鍵盤輔助功能和導航](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 嵌入互動式視頻查看器{#section-6bb5d3c502544ad18a58eafe12a13435}

互動式視訊檢視器已內嵌至托管頁面。 這樣的網頁可以具有靜態版面，或者它可以「響應」，並且在不同設備上或針對不同的瀏覽器窗口大小顯示不同。

為了滿足這些需求，檢視器支援兩種主要操作模式：固定大小內嵌和回應式內嵌。

**關於固定大小嵌入模式和響應式設計嵌入模式**

在內嵌模式中，檢視器會新增至現有網頁，而現有網頁可能已有與檢視器無關的客戶內容。 觀看者通常只佔有網頁的一部分房地產。

主要使用案例是以桌上型電腦或平板電腦裝置為導向的網頁，以及可回應的設計頁面，這些頁面會根據裝置類型自動調整版面。

當檢視器在初始載入後未變更大小時，會使用固定大小內嵌。 對於靜態版面的網頁，此功能是最佳選擇。

回應式設計內嵌假設檢視器需要在執行階段調整大小，以回應其容器`DIV`的大小變更。 最常見的使用案例是在使用彈性頁面版面的網頁中新增檢視器。

在回應式設計內嵌模式中，檢視器的運作方式會因網頁大小其容器`DIV`而有所不同。 如果網頁僅設定容器的寬度`DIV`，保持高度不受限制，則檢視器會根據所使用資產的外觀比例自動選擇其高度。 此功能可確保資產完全符合檢視，而無需邊框上的邊框間距。 此使用案例是使用回應式網頁設計配置架構(例如Bootstrap和Foundation)的網頁中最常見的使用案例。

否則，如果網頁同時設定了查看器容器`DIV`的寬度和高度，則查看器只會填入該區域，並遵循網頁佈局提供的大小。 一個很好的範例是將檢視器嵌入強制回應覆蓋中，其中覆蓋會根據網頁瀏覽器視窗大小來調整大小。

**固定大小嵌入**

您可以執行下列操作，將檢視器新增至網頁：

1. 將檢視器JavaScript檔案新增至您的網頁。
1. 定義容器`DIV`。
1. 設定檢視器大小。
1. 建立和初始化檢視器。

1. 將檢視器JavaScript檔案新增至您的網頁。

   建立檢視器需要在HTML標題中新增指令碼標籤。 使用檢視器API之前，請務必加入[!DNL InterativeVideoViewer.js]。 [!DNL InteractiveVideoViewer.js]檔案位於標準IS-Viewers部署的[!DNL html5/js/]子資料夾下：

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js]

如果檢視器部署在其中一個AdobeDynamic Media Classic伺服器上，且是從相同網域提供，則可使用相對路徑。 否則，您需指定安裝IS-Viewers之其中一個AdobeDynamic Media Classic伺服器的完整路徑。

相對路徑如下所示：

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>僅參考頁面上的主檢視器JavaScript `include`檔案。 請勿在網頁程式碼中參考任何其他JavaScript檔案，這些檔案可能會由檢視器的邏輯在執行階段下載。 尤其是，請勿直接參考檢視器從`/s7viewers`內容路徑（稱為統一SDK `include`）載入的HTML5 SDK `Utils.js`程式庫。 原因在於，`Utils.js`或類似的執行階段檢視器程式庫的位置，是由檢視器的邏輯完全管理，且檢視器版本之間的位置變更。 Adobe不會在伺服器上保留舊版次要檢視器`includes`。
>
>
>因此，將檢視器使用的任何次要JavaScript `include`的直接參考放在頁面上，會在未來部署新產品版本時中斷檢視器的功能。

1. 定義容器`DIV`。

   將空白的`DIV`元素新增至您希望檢視器顯示的頁面。 `DIV`元素必須已定義其ID，因為此ID稍後會傳遞至檢視器API。 DIV的大小是透過CSS指定。

   佔位符`DIV`是定位的元素，這意味著`position` CSS屬性設定為`relative`或`absolute`。

   若要讓全螢幕功能在Internet Explorer中正常運作，請確定DOM中沒有其他元素的堆疊順序比預留位置`DIV`高。

   以下是定義的佔位符`DIV`元素的示例：

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. 設定檢視器大小

   您可以為檢視器設定靜態大小，方法是以絕對單位為`.s7interactivevideoviewer`頂層CSS類別聲明，或使用`stagesize`修飾詞。

   您可以直接在HTML頁面上將大小調整為CSS。 或者，您可以將其放入自訂檢視器CSS檔案中，該檔案稍後會依需求指派給AEM Assets中的檢視器預設集記錄，或使用`style`命令明確傳遞。

   如需使用CSS來設定檢視器樣式的詳細資訊，請參閱[自訂互動式視訊檢視器](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0)。

   以下是在HTML頁面中定義靜態檢視器大小的範例：

   ```
   #s7viewer.s7interactivevideoviewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   您可以在AEM Assets的檢視器預設集記錄中設定`stagesize`修飾詞 — 隨選。 或者，您也可以使用`params`集合的檢視器初始化程式碼，或如「命令參考」區段所述以API呼叫的形式明確傳遞，如下所示：

   ```
   interactivevideoviewer.setParam("stagesize", "640,640");
   ```

   建議使用CSS型方法，此範例中會使用。

1. 建立和初始化檢視器。

   完成上述步驟後，可以建立一個`s7viewers.InteractiveVideoViewer`類的實例，將所有配置資訊傳遞到其建構子，並在查看器實例上調用`init()`方法。 設定資訊會以JSON物件的形式傳遞至建構函式。 此物件至少應有`containerId`欄位，該欄位包含檢視器容器ID的名稱，並巢狀`params` JSON物件，以及檢視器支援的設定參數。

   在此情況下，`params`物件至少必須以`serverUrl`屬性傳遞影像伺服URL，並以`asset`參數傳遞初始資產。 JSON型初始化API可讓您使用單行程式碼、以`videoserverurl`屬性傳遞的視訊伺服器URL、以`asset`參數傳遞的初始資產，以及以`interactivedata`屬性傳遞的互動式資料，來建立和啟動檢視器。 JSON型初始化API可讓您使用一行程式碼來建立和啟動檢視器。

   請務必將檢視器容器新增至DOM，讓檢視器程式碼可以透過其ID來尋找容器元素。 有些瀏覽器會延遲建立DOM，直到網頁結尾為止。 如需最大相容性，請在結尾的`BODY`標籤前，或在內文`onload()`事件上呼叫`init()`方法。

   同時，容器元素還不一定是網頁版面的一部分。 例如，可使用指派給它的`display:none`樣式來隱藏它。 在此情況下，檢視器會延遲其初始化程式，直到網頁將容器元素帶回版面的那一刻為止。 發生此情況時，檢視器載入會自動繼續。

   以下是建立查看器實例的示例，將最小必要配置選項傳遞給建構子並調用`init()`方法。 此範例假設如下：

   * 查看器實例為`interactiveVideoViewer`。
   * 佔位符`DIV`的名稱為`s7viewer`。
   * 影像伺服URL為`https://aodmarketingna.assetsadobe.com/is/image/`。
   * 視訊伺服器URL為`https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna`。
   * 內容URL為`https://aodmarketingna.assetsadobe.com/`。
   * 資產為`/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4`。
   * 互動式資料為`is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt`。

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

   以下程式碼是嵌入固定大小的互動式視訊檢視器的簡單網頁的完整範例：

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

**無限制高度的回應式設計內嵌**

透過回應式設計內嵌，網頁通常會有某種彈性的版面配置，指定檢視器容器`DIV`的執行階段大小。 在下列範例中，假設網頁允許檢視器的容器`DIV`取用40%的網頁瀏覽器視窗大小，使其高度不受限制。 網頁HTML程式碼如下所示：

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

將檢視器新增至此類頁麵類似於固定大小內嵌的步驟。 唯一的差異是您不需要明確定義檢視器大小。

1. 將檢視器JavaScript檔案新增至您的網頁。
1. 定義容器DIV。
1. 建立和初始化檢視器。

上述所有步驟與固定大小嵌入相同。 將容器DIV新增至現有的`"holder"` DIV。 下列程式碼為完整的範例。 注意當瀏覽器調整大小時，檢視器大小會如何變更，以及檢視器外觀比例與資產如何相符。

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

下列範例頁面說明在實際使用中，不受限制高度的回應式設計內嵌：

[即時演示](https://landing.adobe.com/tw/na/dynamic-media/ctir-2755/live-demos.html)

<!-- OLD DEMO LOCATION-KEEP (https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html) -->

**定義寬度和高度的回應式內嵌**

如果定義了寬度和高度的回應式內嵌，則網頁樣式會不同。 它會為`"holder"` DIV提供兩種大小，並在瀏覽器視窗中將其置中。 此外，網頁還將`HTML`和`BODY`元素的大小設定為100%。

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

其餘的嵌入步驟與用於具有不受限制高度的響應嵌入的步驟相同。 產生的範例如下：

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

**使用基於Setter的API嵌入**

您可以使用setter型API和無目標建構函式，而不使用JSON型初始化。 使用此API建構函式時不會採用任何參數，且會使用具有個別JavaScript呼叫的`setContainerId()`、`setParam()`及`setAsset()` API方法指定設定參數。

以下範例說明如何使用固定大小內嵌搭配setter型API:

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
