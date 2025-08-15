---
title: 視訊
description: Video Viewer是視訊播放器，可播放以H.264格式編碼的串流及漸進式視訊。 它是從Dynamic Media Classic或Adobe Experience Manager透過Dynamic Media所提供。
keywords: 回應式
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: fa9727dc-f9e2-4d91-b500-445693dfb6aa
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2333'
ht-degree: 0%

---

# 視訊{#video}

Video Viewer是視訊播放器，可播放以H.264格式編碼的串流及漸進式視訊。 它是從Dynamic Media Classic或Experience Manager透過Dynamic Media所提供。

請參閱[系統需求和先決條件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

同時支援單一視訊和自我調整視訊集。 此外，該檢視器支援使用託管於外部位置的漸進式視訊和HLS資料流。 它設計為可在支援HTML5視訊的案頭和行動網頁瀏覽器上運作。 此檢視器也支援在視訊內容、視訊章節導覽和社群媒體分享工具上方顯示的選擇性隱藏式字幕。

只要基礎系統支援，Video Viewer就會在其預設設定中，使用HLS格式的HTML5串流視訊播放。 在不支援HTML5串流的系統上，檢視器會回到HTML5漸進式視訊傳送。

檢視器型別506。

## 示範URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4](https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4)

## 使用視訊檢視器 {#section-f21ac23d3f6449ad9765588d69584772}

視訊檢視器代表主要JavaScript檔案和一組協助程式檔案。單一JavaScript包含此特定檢視器使用的所有Viewer SDK元件、資產，以及檢視器在執行階段下載的CSS。

您可以使用隨附於IS-Viewers的生產就緒HTML頁面，在快顯視窗模式中使用視訊檢視器。 或者，您可以在內嵌模式中使用檢視器，其中使用檔案化的API將其整合至目標網頁。

設定檢視器外觀的工作與其他檢視器類似。 所有外觀設定都是透過自訂CSS來達成。

檢視所有檢視器通用的[命令參考 — 組態屬性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)和所有檢視器通用的[命令參考 — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 與視訊檢視器互動 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Video Viewer提供一組標準的使用者介面控制項來播放視訊，例如播放/暫停按鈕、視訊筆畫壓感視訊時間泡泡、播放時間/總時間指示器、音量控制、全熒幕按鈕和隱藏式字幕切換。 所有這些控制項都會分組到檢視器使用者介面底部的控制項列中。

在觸控裝置上，音量控制會隱藏在使用者介面中，因為只能使用硬體按鈕來控制音量。

當檢視器在快顯視窗模式下操作時，全熒幕按鈕在使用者介面中無法使用。

當視訊章節啟用時，您可以快速導覽視訊內容。 視訊章節會在視訊筆畫壓感追蹤中顯示為標籤，並在滑鼠滑鼠指向效果上或觸控系統上點一下時顯示章節標題和相關說明。 使用者可以透過選取章節標籤或選取章節說明泡泡來搜尋特定章節。

此檢視器支援觸控式輸入及滑鼠輸入，適用於具有觸控熒幕及滑鼠的Windows裝置。 不過，這項支援僅限Chrome、Internet Explorer 11和Edge網頁瀏覽器。

此檢視器可使用完整的鍵盤。

請參閱[鍵盤協助工具與導覽](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 使用視訊檢視器的社群媒體分享工具 {#section-907d316fe1da4b87abb9775f02464704}

Video Viewer支援社群媒體分享工具。 它們可作為使用者介面中的單一按鈕使用，當使用者按一下或點選共用工具列時，該按鈕會展開至共用工具列。

共用工具列包含支援之每種共用管道型別的圖示，例如Facebook、Twitter、電子郵件共用、內嵌程式碼共用和連結共用。 啟動電子郵件共用、內嵌共用或連結共用工具時，檢視器會顯示模型對話方塊，其中包含對應的資料輸入表單。 呼叫Facebook或Twitter時，檢視器會將使用者從社群媒體服務重新導向至標準共用對話方塊。 當共用工具啟動時，也會自動暫停視訊播放。

因為Web瀏覽器安全限制，所以無法在全熒幕模式中使用共用工具。

## 內嵌視訊檢視器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同的網頁對檢視者的行為有不同的需求。 有時，網頁會提供連結，在選取時會在個別瀏覽器視窗中開啟檢視器。 在其他情況下，需要直接將檢視器內嵌在託管頁面上。 在後一種情況下，網頁可能會有靜態頁面佈局，或使用在不同裝置上或不同瀏覽器視窗大小下顯示不同的回應式設計。 為了滿足這些需求，檢視器支援三種主要操作模式：快顯視窗、固定大小嵌入和回應式設計嵌入。

平板電腦和行動裝置支援在同一頁面上內嵌多個影片。 通常一次只能播放一個視訊。 當使用者開始播放一個影片，然後嘗試播放另一個影片時，會自動暫停第一個影片。 自動暫停的視訊會記住其目前的播放時間，因此使用者可以隨時返回視訊並繼續播放。 此規則唯一的例外是在Android™ 4.x裝置上的Chrome瀏覽器中，該瀏覽器可同時播放視訊。

**關於快顯視窗模式**

在快顯視窗模式中，檢視器會在個別的網頁瀏覽器視窗或標籤中開啟。 它會取用整個瀏覽器視窗區域，並在瀏覽器調整大小或裝置方向變更時進行調整。

此模式在行動裝置中最常見。 網頁會使用`window.open()` JavaScript呼叫、正確設定的`A` HTML元素或任何其他適當的方法載入檢視器。

建議您為快顯視窗操作模式使用現成可用的HTML頁面。 它稱為[!DNL VideoViewer.html]，且位於標準IS-Viewers部署的[!DNL html5/]子資料夾下：

[!DNL <s7viewers_root>/html5/VideoViewer.html]

您可以套用自訂CSS以實現視覺化自訂。

以下是在新視窗中開啟檢視器的HTML程式碼範例：

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4" target="_blank">Open popup viewer</a>
```

**關於固定大小內嵌模式和回應式內嵌模式**

在內嵌模式中，檢視器會新增至現有網頁，其中可能已有某些與檢視器無關的客戶內容。 檢視器通常只會佔用網頁的一部分空間。

主要使用案例是桌上型電腦或平板電腦裝置導向的網頁，以及可依據裝置型別自動調整版面的回應式設計頁面。

當檢視器在初始載入後未變更其大小時，會使用固定大小內嵌。 此選項最適合使用具有靜態頁面配置的網頁。

回應式設計內嵌假設檢視器必須在執行階段調整大小，以回應其容器`DIV`的大小變更。 最常見的使用案例是將檢視器新增到使用彈性頁面配置的網頁。

在回應式設計內嵌模式中，檢視器的行為會因網頁大小其容器`DIV`的方式而異。 如果網頁僅設定容器`DIV`的寬度，而不限制其高度，檢視器會根據所使用資產的外觀比例，自動選擇其高度。 此方法可確保資產完全符合檢視方式，而不會在兩側加上任何邊框間距。 此使用案例最常用於使用回應式設計配置架構(如Bootstrap或Foundation)的網頁。

否則，如果網頁同時設定檢視器容器`DIV`的寬度和高度，則檢視器只會填滿該區域，並遵循網頁配置所提供的大小。 一個好的範例是內嵌檢視器至模式覆蓋圖，其中覆蓋圖會根據網頁瀏覽器視窗的大小而調整。

**固定大小內嵌**

您可以執行下列動作，將檢視器新增至網頁：

1. 正在將viewer JavaScript檔案新增至您的網頁。
1. 定義容器`DIV`。
1. 設定檢視器大小。
1. 正在建立和初始化檢視器。

1. 正在將viewer JavaScript檔案新增至您的網頁。

   建立檢視器需要您在HTML標題中新增指令碼標籤。 在可以使用檢視器API之前，請確定您已包含[!DNL FlyoutViewer.js]。 [!DNL FlyoutViewer.js]檔案位於標準IS-Viewers部署的[!DNL html5/js/]子資料夾下：

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

如果檢視器部署在任一Adobe Dynamic Media Classic伺服器上，且從相同網域提供服務，您就可以使用相對路徑。 否則，請指定已安裝IS-Viewers之其中一個Adobe Dynamic Media Classic伺服器的完整路徑。

相對路徑如下所示：

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/VideoViewer.js"></script>
```

>[!NOTE]
>
>僅參考頁面上的主要檢視器JavaScript `include`檔案。 請勿在網頁程式碼中參考任何其他JavaScript檔案（這些檔案可能由執行階段的檢視器邏輯下載）。 特別是，請勿直接參考檢視器從`Utils.js`內容路徑(所謂整合的HTML `/s7viewers`)載入的SDK5 SDK `include`資料庫。 原因在於`Utils.js`或類似的執行階段檢視器程式庫的位置完全由檢視器的邏輯管理，且位置會在檢視器發行版本之間變更。 Adobe不會在伺服器上保留舊版的次要檢視器`includes`。
>
>
>因此，日後部署新產品版本時，將檢視器使用的任何次要JavaScript `include`的直接參照放在頁面上，會中斷檢視器功能。

1. 定義容器DIV。

   新增空的DIV元素至要顯示檢視器的頁面。 DIV元素必須定義其ID，因為此ID稍後會傳遞至檢視器API。 DIV的大小是透過CSS指定。

   預留位置DIV是定位元素，表示`position` CSS屬性設定為`relative`或`absolute`。

   請確定Internet Explorer中的全熒幕功能可正常運作。 確認DOM中沒有其他元素的棧疊順序高於預留位置DIV。

   以下為已定義預留位置DIV元素的範例：

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. 設定檢視器大小

   您可以透過以絕對單位宣告`.s7videoviewer`最上層CSS類別的檢視器，或使用修飾元`stagesize`來設定檢視器的靜態大小。

   您可以在HTML頁面或自訂檢視器CSS檔案中將CSS的大小調整放入。 之後會將其指派給Dynamic Media Classic中的檢視器預設集記錄，或使用style命令明確傳遞。

   請參閱[自訂視訊檢視器](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e)，以取得使用CSS設定檢視器樣式的詳細資訊。

   以下是在HTML頁面中定義靜態檢視器大小的範例：

   ```html {.line-numbers}
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   您可以在Dynamic Media Classic的檢視器預設集記錄中設定`stagesize`修飾元，或透過`params`集合的檢視器初始化程式碼明確傳遞。 或者，如命令參考區段中所述，作為API呼叫，如下所示：

   ```html {.line-numbers}
   videoViewer.setParam("stagesize", "640,480");
   ```

   此範例建議您使用以CSS為基礎的方法。

1. 正在建立和初始化檢視器。

   完成上述步驟後，您會建立`s7viewers.VideoViewer`類別的執行個體、將所有組態資訊傳遞至其建構函式，並在檢視器執行個體上呼叫`init()`方法。 組態資訊會以JSON物件的形式傳遞至建構函式。 此物件至少應有`containerId`欄位，其內含檢視器容器ID的名稱，以及含有檢視器支援之組態引數的巢狀`params` JSON物件。 在此案例中，`params`物件必須至少將影像伺服URL傳遞為`serverUrl`屬性、將視訊伺服器URL傳遞為`videoserverurl`屬性，並將初始資產傳遞為`asset`引數。 JSON型初始化API可讓您使用一行程式碼來建立和啟動檢視器。

   請務必將檢視器容器新增至DOM，讓檢視器程式碼可依其ID尋找容器元素。 有些瀏覽器會延遲建立DOM，直到網頁結尾為止。 為達到最大相容性，請在結尾的`init()`標籤前面或內文`BODY`事件上呼叫`onload()`方法。

   同時，容器元素也不一定屬於網頁版面配置的一部分。 例如，可以使用指派給它的`display:none`樣式來隱藏它。 在此情況下，檢視器會延遲其初始化程式，直到網頁將容器元素帶回版面配置為止。 當此動作發生時，檢視器載入會自動繼續。

   以下是建立檢視器執行個體、將最低必要組態選項傳遞給建構函式，以及呼叫`init()`方法的範例。 此範例假設`videoViewer`是檢視器執行個體，`s7viewer`是預留位置的名稱`DIV`，[!DNL http://s7d1.scene7.com/is/image/]是影像伺服URL，[!DNL http://s7d1.scene7.com/is/content/]是視訊伺服器URL，而[!DNL Scene7SharedAssets/Glacier_Climber_MP4]是資產。

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var videoViewer = new s7viewers.VideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   ```

   下列程式碼為將視訊檢視器嵌入固定大小的簡單網頁的完整範例：

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
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
   var videoViewer = new s7viewers.VideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html> 
   ```

**高度不受限制的回應式設計內嵌**

透過內嵌回應式設計，網頁通常會有某種彈性的配置，可指定檢視器容器`DIV`的執行階段大小。 在此範例中，假設網頁允許檢視器的容器`DIV`取得網頁瀏覽器視窗大小的40%，其高度不受限制。 網頁HTML程式碼如下所示：

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

將檢視器新增到這類頁麵類似於嵌入固定大小；唯一的區別是您不需要明確定義檢視器大小。

1. 正在將viewer JavaScript檔案新增至您的網頁。
1. 定義容器DIV。
1. 正在建立和初始化檢視器。

上述所有步驟與內嵌固定大小相同。 將容器`DIV`新增至現有的「持有者」`DIV`。 下列程式碼為完整的範例。 您可以檢視瀏覽器調整大小時檢視器大小的變更，以及檢視器外觀比例與資產的相符情形。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
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
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

以下範例頁面說明高度不受限制的回應式設計內嵌在實際應用中的更多效果：

[即時示範](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[備用示範位置](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html?lang=zh-Hant)

**定義寬度和高度的回應式設計內嵌**

如果有已定義寬度和高度的回應式設計內嵌，則網頁樣式會不同；它會將「`DIV`」的大小提供給「托架」，並將它置中在瀏覽器視窗中。 此外，網頁會將`HTML`和`BODY`專案的大小設定為100%：

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

其餘的內嵌步驟與高度不受限制的回應式設計內嵌相同。 產生的範例如下：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
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
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

**使用Setter型API進行內嵌**

除了使用JSON型初始化之外，也可以使用setter型API和no-args建構函式。 使用該API，建構函式不會接受任何引數，而且設定引數是使用`setContainerId()`、`setParam()`和`setAsset()` API方法搭配個別的JavaScript呼叫所指定。

下列範例說明使用setter型API嵌入固定大小的內容：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
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
var videoViewer = new s7viewers.VideoViewer(); 
videoViewer.setContainerId("s7viewer"); 
videoViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
videoViewer.setParam("videoserverurl", "http://s7d1.scene7.com/is/content/"); 
videoViewer.setAsset("Scene7SharedAssets/Glacier_Climber_MP4"); 
videoViewer.init(); 
</script> 
</body> 
</html> 
```
