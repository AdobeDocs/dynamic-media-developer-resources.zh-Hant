---
title: 互動視訊
description: 互動式視訊檢視器是一種視訊播放器，可播放以H.264格式編碼的串流及漸進式視訊。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: e54b0b1f-b015-4592-82e2-99f5080543e3
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2180'
ht-degree: 0%

---

# 互動視訊{#interactive-video}

互動式視訊檢視器是一種視訊播放器，可播放以H.264格式編碼的串流及漸進式視訊。

檢視器也會在視訊內容旁顯示互動式產品色票。 同時支援單一視訊和自我調整視訊集。 它設計為可在支援HTML5視訊的桌上型電腦和行動網頁瀏覽器上運作。 檢視器支援在視訊內容、視訊章節導覽和社交分享工具頂端顯示的選擇性隱藏式字幕。 此檢視器的用途是協助您實作「可購物視訊」體驗。 也就是說，使用者可以選取與特定視訊時區相關聯的色票，並重新導向至客戶網站上的快速檢視或產品詳細資料頁面。

檢視器型別為510。

## 示範URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/glacier/InteractiveVideoViewerDemo.html?lang=zh-Hant](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/glacier/InteractiveVideoViewerDemo.html?lang=zh-Hant)

與

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/AXIS/index.html?lang=zh-Hant](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/AXIS/index.html?lang=zh-Hant)

## 系統要求 {#section-b7270cc4290043399681dc504f043609}

請參閱[系統需求](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

## 使用互動式視訊檢視器 {#section-e6c68406ecdc4de781df182bbd8088b4}

互動式視訊檢視器代表主要JavaScript檔案和一組由檢視器在執行階段下載的Helper檔案。 單一JavaScript包含在此特定檢視器、資產和CSS使用的所有檢視器SDK元件中。

互動式視訊檢視器可使用隨影像伺服檢視器提供的生產就緒HTML頁面，以快顯視窗模式使用。 它也可用於內嵌模式，其中使用檔案化API將其整合到目標網頁中。

設定和外觀設定類似於本指南中描述的其他檢視器。 所有外觀設定都是透過自訂(CSS)階層式樣式表來達成。

檢視所有檢視器通用的[命令參考 — 組態屬性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)和所有檢視器通用的[命令參考 — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 與互動式視訊檢視器互動 {#section-642e66ca38cd4032992840ec6c0b0cd2}

互動式視訊檢視器提供一組標準的使用者介面控制項供視訊播放之用，例如播放/暫停按鈕、視訊筆畫壓感器、視訊時間泡泡、播放時間/總時間指示器、音量控制、全熒幕按鈕和隱藏式字幕切換。 所有這些控制項都會分組到直接位於主檢視下的控制項列中。

在觸控裝置上，音量控制會隱藏在使用者介面中，因為只能使用裝置的硬體按鈕來控制音量。

當檢視器在快顯視窗模式下操作時，全熒幕按鈕在使用者介面中無法使用。

檢視器會在視訊檢視區域的右側，顯示含有互動色票的面板。 色票清單會在視訊播放時自動前進，以便顯示與目前視訊區域對應的色票。 在製作期間，按一下或點選色票會觸發與此色票相關聯的動作。 根據您的設定方式，觸發器可能會重新導向至網站上的不同頁面。 或者，它可能會將產品資訊傳回網頁邏輯，繼而觸發顯示相關產品內容的Quickview開啟。

當視訊章節啟用時，您可以快速導覽視訊內容。 視訊章節在視訊筆畫壓感追蹤中會顯示為標籤，並在滑鼠指向效果時顯示章節標題和說明（或在觸控系統上點一下滑鼠指向效果時顯示）。 客戶可以按一下章節標籤或點選章節說明泡泡圖，以「搜尋」特定章節。

檢視器也支援各種社群媒體分享工具。 它們可作為使用者介面中的單一按鈕使用，當使用者按一下或點選共用工具列時，該按鈕會展開至共用工具列。 共用工具列包含每個支援共用管道型別的圖示，例如Facebook、Twitter、電子郵件共用、內嵌程式碼共用和連結共用。 啟動電子郵件共用、內嵌共用或連結共用工具時，檢視器會顯示模型對話方塊，其中包含對應的資料輸入表單。 呼叫Facebook或Twitter時，檢視器會將使用者從社群媒體服務重新導向至標準共用對話方塊。 此外，當共用工具啟動時，視訊播放會自動暫停。 因為Web瀏覽器安全限制，所以無法在全熒幕模式中使用共用工具。

檢視器可使用完整的鍵盤。 請參閱[鍵盤協助工具與導覽](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 內嵌互動式視訊檢視器 {#section-6bb5d3c502544ad18a58eafe12a13435}

互動式視訊檢視器內嵌於託管頁面。 這類網頁可能具有靜態版面，也可能是「回應式」的，且在不同裝置或不同瀏覽器視窗大小中顯示時不同。

為因應這些需求，檢視器支援兩種主要操作模式：固定大小內嵌和回應式內嵌。

**關於固定大小內嵌模式和回應式設計內嵌模式**

在內嵌模式中，檢視器會新增至現有網頁，其中可能已有某些與檢視器無關的客戶內容。 檢視器通常只會佔用網頁的一部分空間。

主要使用案例是針對桌上型電腦或平板電腦裝置的網頁，以及可依據裝置型別自動調整版面的回應式設計頁面。

當檢視器在初始載入後未變更其大小時，會使用固定大小內嵌。 此功能為靜態佈局網頁的最佳選擇。

回應式設計內嵌假設檢視器在執行階段需要調整大小以回應其容器`DIV`的大小變更。 最常見的使用案例是將檢視器新增到使用彈性頁面配置的網頁。

在回應式設計內嵌模式中，檢視器的行為會因網頁大小其容器`DIV`的方式而異。 如果網頁僅設定容器`DIV`的寬度，而不限制其高度，檢視器會根據所使用資產的外觀比例，自動選擇其高度。 此功能可確保資產完全符合檢視方式，且兩側不會有任何邊框間距。 此使用案例最常用於使用回應式網頁設計配置架構(例如Bootstrap和Foundation)的網頁。

否則，如果網頁同時設定檢視器容器`DIV`的寬度和高度，則檢視器只會填滿該區域，並遵循網頁配置所提供的大小。 一個好的範例是內嵌檢視器至強制回應覆蓋圖，其中覆蓋圖會根據網頁瀏覽器視窗大小而調整。

**固定大小內嵌**

您可以執行下列動作，將檢視器新增至網頁：

1. 正在將viewer JavaScript檔案新增至您的網頁。
1. 定義容器`DIV`。
1. 設定檢視器大小。
1. 正在建立和初始化檢視器。

1. 正在將viewer JavaScript檔案新增至您的網頁。

   建立檢視器需要您在HTML標題中新增指令碼標籤。 在可以使用檢視器API之前，請確定您已包含[!DNL InterativeVideoViewer.js]。 [!DNL InteractiveVideoViewer.js]檔案位於標準IS-Viewers部署的[!DNL html5/js/]子資料夾下：

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js]

如果檢視器部署在任一Adobe Dynamic Media Classic伺服器上，且從相同網域提供服務，您就可以使用相對路徑。 否則，請指定已安裝IS-Viewers之其中一個Adobe Dynamic Media Classic伺服器的完整路徑。

相對路徑如下所示：

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>僅參考頁面上的主要檢視器JavaScript `include`檔案。 請勿在網頁程式碼中參考任何其他JavaScript檔案（這些檔案可能由執行階段的檢視器邏輯下載）。 特別是，請勿直接參考檢視器從`/s7viewers`內容路徑（所謂整合SDK `include`）載入的HTML5 SDK `Utils.js`資料庫。 原因在於`Utils.js`或類似的執行階段檢視器程式庫的位置完全由檢視器的邏輯管理，且位置會在檢視器發行版本之間變更。 Adobe不會在伺服器上保留舊版的次要檢視器`includes`。
>
>
>因此，日後部署新產品版本時，將檢視器使用的任何次要JavaScript `include`的直接參照放在頁面上，會中斷檢視器功能。

1. 定義容器`DIV`。

   新增空的`DIV`元素至您要檢視器出現的頁面。 `DIV`專案必須定義其ID，因為此ID稍後會傳遞至檢視器API。 DIV的大小是透過CSS指定。

   預留位置`DIV`是定位元素，表示`position` CSS屬性設定為`relative`或`absolute`。

   若要讓全熒幕功能在Internet Explorer中正常運作，請確定DOM中沒有其他元素的棧疊順序高於預留位置`DIV`。

   以下是已定義的預留位置`DIV`元素的範例：

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. 設定檢視器大小

   您可以透過以絕對單位宣告`.s7interactivevideoviewer`頂層CSS類別的檢視器，或使用`stagesize`修飾元來設定檢視器的靜態大小。

   您可以直接在HTML頁面上調整CSS的大小。 或者，您可以將其放入自訂檢視器CSS檔案中，稍後再將該檔案指派給Adobe Experience Manager Assets中的檢視器預設集記錄（隨選），或使用`style`命令明確傳遞。

   請參閱[自訂互動式視訊檢視器](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0)，以取得使用CSS設定檢視器樣式的詳細資訊。

   以下是在「HTML」頁面中定義靜態檢視器大小的範例：

   ```html {.line-numbers}
   #s7viewer.s7interactivevideoviewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   您可以在Experience Manager Assets的檢視器預設集記錄中設定`stagesize`修飾元 — 隨選。 或者，您可以使用`params`集合的檢視器初始化程式碼來明確傳遞它，或以API呼叫的形式傳遞，如Command Reference區段中所述，如下所示：

   ```html {.line-numbers}
   interactivevideoviewer.setParam("stagesize", "640,640");
   ```

   此範例建議您使用以CSS為基礎的方法。

1. 正在建立和初始化檢視器。

   完成上述步驟後，您會建立`s7viewers.InteractiveVideoViewer`類別的執行個體、將所有組態資訊傳遞至其建構函式，並在檢視器執行個體上呼叫`init()`方法。 組態資訊會以JSON物件的形式傳遞至建構函式。 此物件至少應有`containerId`欄位，其包含檢視器容器ID的名稱，以及含有檢視器支援之組態引數的巢狀`params` JSON物件。

   在此情況下，`params`物件必須至少將影像伺服URL傳遞為`serverUrl`屬性，並將初始資產傳遞為`asset`引數。 JSON型初始化API可讓您使用一行程式碼、以`videoserverurl`屬性傳遞的視訊伺服器URL、以`asset`引數傳遞的初始資產，以及以`interactivedata`屬性傳遞的互動式資料，來建立及啟動檢視器。 JSON型初始化API可讓您使用一行程式碼來建立和啟動檢視器。

   請務必將檢視器容器新增至DOM，讓檢視器程式碼可依其ID尋找容器元素。 有些瀏覽器會延遲建立DOM，直到網頁結尾為止。 為達到最大相容性，請在結尾的`BODY`標籤前面或內文`onload()`事件上呼叫`init()`方法。

   同時，容器元素也未必是網頁配置的一部分。 例如，可以使用指派給它的`display:none`樣式來隱藏它。 在此情況下，檢視器會延遲其初始化程式，直到網頁將容器元素帶回版面配置為止。 之後，檢視器會自動繼續載入。

   以下是建立檢視器執行個體、將最低必要組態選項傳遞至建構函式並呼叫`init()`方法的範例。 此範例假設以下情況：

   * 檢視器執行個體是`interactiveVideoViewer`。
   * 預留位置`DIV`的名稱為`s7viewer`。
   * 影像伺服URL為`https://aodmarketingna.assetsadobe.com/is/image/`。
   * 視訊伺服器URL是`https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna`。
   * 內容URL為`https://aodmarketingna.assetsadobe.com/`。
   * 資產為`/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4`。
   * 互動式資料為`is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt`。

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

   下列程式碼為將互動式視訊檢視器嵌入固定大小的簡單網頁的完整範例：

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

**高度不受限制的回應式設計內嵌**

透過回應式設計內嵌，網頁通常會有某種彈性的配置，可指定檢視器容器`DIV`的執行階段大小。 對於下列範例，假設網頁允許檢視器的容器`DIV`取得網頁瀏覽器視窗大小的40%，其高度不受限制。 網頁HTML程式碼如下所示：

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

將檢視器新增至這類頁面，類似於固定大小內嵌的步驟。 唯一的區別是您不需要明確定義檢視器大小。

1. 正在將viewer JavaScript檔案新增至您的網頁。
1. 定義容器DIV。
1. 正在建立和初始化檢視器。

上述所有步驟與內嵌固定大小相同。 將容器DIV新增至現有的`"holder"` DIV。 下列程式碼為完整的範例。 請注意瀏覽器調整大小時檢視器大小的變化，以及檢視器外觀比例與資產的相符情形。

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

以下範例頁面說明高度不受限制的回應式設計內嵌在實際應用中的更多情況：

[即時示範](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[備用示範位置](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html?lang=zh-Hant)

已定義寬度和高度的&#x200B;**回應式內嵌**

如果有已定義寬度和高度的回應式內嵌，則網頁樣式會不同。 它同時提供大小給`"holder"` DIV，並將它置中於瀏覽器視窗中。 此外，網頁會將`HTML`和`BODY`專案的大小設定為100%。

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

其餘的內嵌步驟與高度不受限制的回應式內嵌步驟相同。 產生的範例如下：

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

**使用Setter型API內嵌**

除了使用JSON型初始化之外，也可以使用setter型API和no-args建構函式。 使用此API建構函式不會接受任何引數，而設定引數是使用`setContainerId()`、`setParam()`和`setAsset()` API方法搭配個別的JavaScript呼叫所指定。

下列範例說明如何將固定大小內嵌與setter型API搭配使用：

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
