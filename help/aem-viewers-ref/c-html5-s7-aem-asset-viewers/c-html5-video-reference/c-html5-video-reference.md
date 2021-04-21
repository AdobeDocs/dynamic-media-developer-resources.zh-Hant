---
description: 視訊檢視器是視訊播放器，可播放以H.264格式編碼的串流和漸進式視訊。 它由Dynamic Media經典或AEMDynamic Media提供。
keywords: 回應
solution: Experience Manager
title: 視訊
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '2383'
ht-degree: 0%

---


# 視訊{#video}

視訊檢視器是視訊播放器，可播放以H.264格式編碼的串流和漸進式視訊。 它由Dynamic Media經典或AEMDynamic Media提供。

請參閱[系統需求和先決條件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

同時支援單一視訊和最適化視訊集。 此外，檢視器還支援使用外部位置上裝載的漸進式視訊和HLS串流。 它可在支援HTML5視訊的案頭和行動網頁瀏覽器上運作。 此檢視器也支援視訊內容、視訊章節導覽和社交媒體分享工具之上顯示的選擇性隱藏字幕。

視訊檢視器會在基礎系統支援時，使用HLS格式的HTML5串流視訊播放預設組態。 在不支援HTML5串流的系統上，檢視器會退回HTML5漸進式視訊傳送。

檢視器類型506。

## 示範URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4](https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4)

## 使用視訊檢視器{#section-f21ac23d3f6449ad9765588d69584772}

視訊檢視器代表主要JavaScript檔案和一組輔助檔案——單一JavaScript包含在檢視器SDK元件中，此特定檢視器使用的所有檢視器SDK元件、資產，以及檢視器在執行時期下載的CSS。

您可以使用隨IS檢視器提供的可立即生產使用的HTML頁面，在快顯模式中使用視訊檢視器。 或者，您可以在內嵌模式中使用檢視器，在此模式中，檢視器會使用檔案化的API整合至目標網頁。

設定檢視器及設定其外觀的工作與其他檢視器類似。 所有外觀設定都是透過自訂CSS來完成。

請參閱所有檢視器通用的[命令參考——設定屬性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)和[所有檢視器通用的命令參考- URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 與視訊檢視器互動{#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

視訊檢視器提供一組標準的視訊播放使用者介面控制項，例如播放／暫停按鈕、視訊畫布視訊時間泡泡、播放時間／總時間指示器、音量控制、全螢幕按鈕和隱藏字幕切換。 所有這些控制項都會分組在檢視器使用者介面底部的控制列中。

在觸控裝置上，音量控制會從使用者介面中隱藏，因為只有使用硬體按鈕才能控制音量。

當檢視器在快顯模式下運作時，使用者介面中就無法使用全螢幕按鈕。

在啟動視訊旁白時，可快速導覽視訊內容。 視訊章節會在視訊筆畫軌道中顯示為標籤，並在滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑鼠滑 用戶可以通過按一下章節標籤或點選章節描述泡泡來查找特定章節。

檢視器支援在Windows裝置上使用觸控螢幕和滑鼠的觸控輸入和滑鼠輸入。 不過，這項支援僅限Chrome、Internet Explorer 11和Edge網頁瀏覽器。

此檢視器可完全透過鍵盤存取。

請參閱[鍵盤協助功能和導覽](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 使用視訊檢視器{#section-907d316fe1da4b87abb9775f02464704}的社交媒體分享工具

視訊檢視器支援社交媒體分享工具。使用者介面中的單一按鈕可供使用，當使用者點選或點選時，會展開為分享工具列。

共用工具列包含每種支援分享管道類型的圖示，例如Facebook、Twitter、電子郵件分享、內嵌代碼分享和連結分享。 當啟用電子郵件共用、內嵌共用或連結共用工具時，檢視器會顯示包含對應資料輸入表單的強制對話方塊。 呼叫Facebook或Twitter時，檢視器會將使用者從社交媒體服務重新導向至標準共用對話方塊。 當共用工具啟動時，也會自動暫停視訊播放。

由於網頁瀏覽器的安全性限制，共用工具無法在全螢幕模式下使用。

## 內嵌視訊檢視器{#section-6bb5d3c502544ad18a58eafe12a13435}

不同的網頁對檢視器行為有不同的需求。 有時網頁會提供連結，當點按時會在個別的瀏覽器視窗中開啟檢視器。 在其他情況下，必須將檢視器直接內嵌在代管頁面上。 在後一種情況下，網頁可能具有靜態頁面版面，或使用不同裝置或不同瀏覽器視窗大小顯示不同的互動式設計。 為滿足這些需求，檢視器支援三種主要作業模式：彈出畫面、固定大小內嵌和回應式設計內嵌。

平板電腦和行動裝置支援將多個影片內嵌在相同頁面上。 在大多數情況下，一次只能播放一個視訊。 當使用者開始播放一個視訊，然後嘗試播放另一個視訊時，會自動暫停第一個視訊。 自動暫停的視訊會記住其目前的播放時間，因此使用者可隨時回到視訊並繼續播放。 此規則的唯一例外是在Android 4.x裝置上的Chrome瀏覽器中，可以同時播放視訊。

**關於彈出式模式**

在快顯模式中，檢視器會在個別的網頁瀏覽器視窗或標籤中開啟。 它會佔用整個瀏覽器視窗區域，並在調整瀏覽器大小或變更裝置方向時進行調整。

此模式是行動裝置最常見的模式。 網頁會使用`window.open()` JavaScript呼叫、正確設定的`A` HTML元素或任何其他適當的方法載入檢視器。

建議您使用現成可用的HTML頁面來建立快顯作業模式。 它稱為[!DNL VideoViewer.html]，位於標準IS-Viewer部署的[!DNL html5/]子資料夾下：

[!DNL <s7viewers_root>/html5/VideoViewer.html]

您可以套用自訂CSS，以實現視覺化自訂。

以下是在新視窗中開啟檢視器的HTML程式碼範例：

```
<a href="http://s7d1.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4" target="_blank">Open popup viewer</a>
```

**關於固定大小的嵌入模式和自適應嵌入模式**

在內嵌模式中，檢視器會新增至現有的網頁，而現有網頁可能已有與檢視器無關的客戶內容。 檢視器通常只佔據網頁的部分空間。

主要使用案例是面向桌上型電腦或平板電腦裝置的網頁，以及可根據裝置類型自動調整版面的自適應設計頁面。

當檢視器在初始載入後未變更其大小時，會使用固定大小內嵌。 此選項最適合具有靜態頁面版面的網頁。

回應式設計內嵌假設檢視器可能需要在執行時期調整大小，以回應其容器`DIV`的大小變更。 最常見的使用案例是將檢視器新增至使用彈性頁面版面的網頁。

在回應式設計內嵌模式中，檢視器的運作方式會因網頁大小（容器`DIV`）而異。 如果網頁僅設定容器的寬度`DIV`，而不限制其高度，檢視器會根據所使用資產的寬高比自動選擇其高度。 此方法可確保資產完美地貼合至檢視中，而不會在側邊產生任何間距。 此使用案例最常用於使用互動式設計版面架構(例如Bootstrap、基礎等)的網頁。

否則，如果網頁同時設定檢視器容器`DIV`的寬度和高度，檢視器只會填滿該區域，並遵循網頁版面提供的大小。 一個很好的例子是將檢視器內嵌至模態覆蓋，其中覆蓋會根據網頁瀏覽器視窗的大小來調整大小。

**固定大小內嵌**

您可執行下列動作，將檢視器新增至網頁：

1. 將檢視器JavaScript檔案新增至您的網頁。
1. 定義容器`DIV`。
1. 設定檢視器大小。
1. 建立和初始化檢視器。

1. 將檢視器JavaScript檔案新增至您的網頁。

   建立檢視器時，您必須在HTML標題中新增指令碼標籤。 請務必加入[!DNL FlyoutViewer.js]，才能使用檢視器API。 [!DNL FlyoutViewer.js]檔案位於標準IS-Viewer部署的[!DNL html5/js/]子資料夾下：

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

如果檢視器部署在其中一個Adobe的Dynamic Media經典伺服器上，且是從相同網域提供，則可使用相對路徑。 否則，您將指定到安裝IS-Viewer的AdobeDynamic Media經典伺服器之一的完整路徑。

相對路徑如下所示：

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/VideoViewer.js"></script>
```

>[!NOTE]
>
>您只應在頁面上參考主要檢視器JavaScript `include`檔案。 您不應在網頁程式碼中參考檢視器邏輯在執行時期中可能下載的任何其他JavaScript檔案。 尤其是，請勿直接參考檢視器從`/s7viewers`內容路徑載入的HTML5 SDK `Utils.js`程式庫（稱為統一SDK `include`）。 原因是`Utils.js`或類似的執行時期檢視器程式庫的位置完全由檢視器的邏輯管理，而檢視器版本間的位置也會變更。 Adobe不會在伺服器上保留舊版次要檢視器`includes`。
>
>
>因此，將檢視器使用的任何次要JavaScript `include`直接參考放在頁面上，將來部署新產品版本時，檢視器功能會中斷。

1. 定義容器DIV。

   將空的DIV元素新增至您要檢視器顯示的頁面。 DIV元素必須定義其ID，因為此ID稍後會傳遞至檢視器API。 DIV的大小是透過CSS指定的。

   預留位置DIV是定位的元素，這表示`position` CSS屬性設為`relative`或`absolute`。

   確保全螢幕功能在Internet Explorer中正常運作。 檢查以確定DOM中沒有其他元素的堆疊順序高於預留位置DIV。

   以下是已定義預留位置DIV元素的範例：

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. 設定檢視器大小

   您可以設定檢視器的靜態大小，方法是以絕對單位聲明`.s7videoviewer`頂層CSS類別，或使用修飾詞`stagesize`。

   CSS中的大小可直接放在HTML頁面上，或自訂檢視器CSS檔案中，此檔案稍後會指派給Dynamic Media·Classic中的檢視器預設記錄，或使用樣式命令明確傳遞。

   如需使用CSS設定檢視器樣式的詳細資訊，請參閱[自訂視訊檢視器](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e)。

   以下是在HTML頁面中定義靜態檢視器大小的範例：

   ```
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   您可以在Dynamic MediaClassic的檢視器預設記錄中設定`stagesize`修飾元，或以`params`系列的檢視器初始化程式碼明確傳遞它，或以指令參考區段中所述的API呼叫傳遞，如下所述：

   ```
   videoViewer.setParam("stagesize", "640,480");
   ```

   建議使用以CSS為基礎的方法，並在此範例中使用。

1. 建立和初始化檢視器。

   完成上述步驟後，您將建立一個`s7viewers.VideoViewer`類的實例，將所有配置資訊傳遞給其建構子，並在查看器實例上調用`init()`方法。 設定資訊會以JSON物件的形式傳遞至建構函式。 至少，此物件應具有`containerId`欄位，此欄位包含檢視器容器ID的名稱，並巢狀內嵌`params` JSON物件，檢視器支援設定參數。 在這種情況下，`params`物件至少必須有以`serverUrl`屬性傳遞的影像伺服URL、以`videoserverurl`屬性傳遞的視訊伺服器URL，以及以`asset`參數傳遞的初始資產。 以JSON為基礎的初始化API可讓您使用一行程式碼來建立和啟動檢視器。

   請務必將檢視器容器新增至DOM，如此檢視器程式碼就能依其ID找到容器元素。 有些瀏覽器會延遲建立DOM，直到網頁結束為止。 為獲得最大相容性，請在`BODY`結束標籤之前或在主體`onload()`事件上調用`init()`方法。

   同時，容器元素也不一定是網頁版面的一部分。 例如，它可能會使用指派給它的`display:none`樣式進行隱藏。 在此情況下，檢視器會延遲其初始化程式，直到網頁將容器元素帶回版面為止。 發生此情況時，檢視器載入會自動繼續。

   以下是建立檢視器例項、將最小必要組態選項傳遞至建構函式，以及呼叫`init()`方法的範例。 此範例假設`videoViewer`是檢視器例項，`s7viewer`是預留位置`DIV`的名稱，[!DNL http://s7d1.scene7.com/is/image/]是影像伺服URL,[!DNL http://s7d1.scene7.com/is/content/]是視訊伺服器URL，而[!DNL Scene7SharedAssets/Glacier_Climber_MP4]是資產。

   ```
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

   以下程式碼是內嵌固定大小視訊檢視器之平凡網頁的完整範例：

   ```
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

**不受高度限制的自適應設計內嵌**

有了互動式設計內嵌功能，網頁通常就有某種彈性的版面配置，指定檢視器容器`DIV`的執行時期大小。 在此範例中，假設網頁允許檢視器的容器`DIV`取用40%的網頁瀏覽器視窗大小，並保留其高度不受限制。 網頁HTML程式碼如下所示：

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

將檢視器加入此類頁面，與固定大小的內嵌十分類似；唯一的區別是您不需要明確定義檢視器大小。

1. 將檢視器JavaScript檔案新增至您的網頁。
1. 定義容器DIV。
1. 建立和初始化檢視器。

上述所有步驟都與固定大小內嵌相同。 將容器`DIV`新增至現有的&quot; holder&quot; `DIV`。 以下程式碼為完整範例。 您可以看到在調整瀏覽器大小時，檢視器大小的變更，以及檢視器外觀比例與資產的相符程度。

```
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

下列範例頁面說明如何實際使用高度不受限制的自適應設計內嵌功能：

[即時展示](https://landing.adobe.com/tw/na/dynamic-media/ctir-2755/live-demos.html)

<!-- KEEP (https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html) -->

**定義寬度和高度的自適應設計內嵌**

在定義了寬度和高度的自適應設計嵌入時，網頁的樣式不同；它為&quot;holder&quot; `DIV`提供兩種大小，並將它們置於瀏覽器視窗中。 此外，網頁還將`HTML`和`BODY`元素的大小設為100%:

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

其餘的嵌入步驟與高度不受限制的自適應設計嵌入步驟相同。 產生的範例如下：

```
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

您可以使用setter-based API和no-args建構函式，而不是使用JSON型初始化。 使用該API時，建構函式不會採用任何參數，而設定參數是使用`setContainerId()`、`setParam()`和`setAsset()` API方法，並使用個別的JavaScript呼叫來指定。

下列範例說明使用setter-based API進行固定大小內嵌：

```
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

