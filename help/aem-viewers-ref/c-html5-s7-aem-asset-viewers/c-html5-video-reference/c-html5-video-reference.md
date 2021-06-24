---
description: 視訊檢視器是視訊播放器，會播放以H.264格式編碼的串流和漸進式視訊。 是由Dynamic Media Classic或AEM Dynamic Media提供。
keywords: 回應式
solution: Experience Manager
title: 視訊
feature: Dynamic Media Classic，檢視器， SDK/API，影片
role: Developer,Business Practitioner
exl-id: fa9727dc-f9e2-4d91-b500-445693dfb6aa
source-git-commit: e6ff4ed80b22e10fc2bd3fac0f4e39bbf5148f8e
workflow-type: tm+mt
source-wordcount: '2388'
ht-degree: 0%

---

# 視訊{#video}

視訊檢視器是視訊播放器，會播放以H.264格式編碼的串流和漸進式視訊。 是由Dynamic Media Classic或AEM Dynamic Media提供。

請參閱[系統要求和必要條件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

支援單一視訊和最適化視訊集。 此外，檢視器支援使用裝載在外部位置的漸進式視訊和HLS資料流。 它專為支援HTML5視訊的案頭和行動網頁瀏覽器所設計。 此檢視器也支援視訊內容、視訊章節導覽和社交媒體分享工具頂端顯示的可選隱藏式字幕。

只要基礎系統支援，視訊檢視器就會在其預設設定中使用HTML5串流視訊播放（HLS格式）。 在不支援HTML5串流的系統上，檢視器會回復為HTML5漸進式視訊傳送。

檢視器類型506。

## 示範URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4](https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4)

## 使用視訊檢視器 {#section-f21ac23d3f6449ad9765588d69584772}

視訊檢視器代表主要JavaScript檔案和一組協助檔案 — 單一JavaScript包含，以及該特定檢視器使用的所有檢視器SDK元件、資產，以及檢視器在執行階段下載的CSS。

您可以使用隨IS檢視器提供的生產就緒HTML頁面，以快顯模式使用視訊檢視器。 或者，您可以在內嵌模式中使用檢視器，透過記錄的API將其整合至目標網頁。

設定檢視器和設定檢視器外觀的任務與其他檢視器類似。 所有外觀設定都是透過自訂CSS來達成。

請參閱所有檢視器通用的[命令參考 — 設定屬性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)和所有檢視器通用的[命令參考 — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 與視訊檢視器互動 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

視訊檢視器提供一組用於視訊播放的標準使用者介面控制項，例如播放/暫停按鈕、視訊清除程式視訊時間泡泡、播放時間/總時間指標、音量控制、全螢幕按鈕和隱藏式字幕切換。 所有這些控制項都會分組到檢視器使用者介面底部的控制列中。

在觸摸設備上，音量控制在用戶介面中隱藏，因為只能使用硬體按鈕控制音量。

檢視器在快顯模式中運作時，使用者介面中無法使用全螢幕按鈕。

啟動視訊分段時，可快速導覽視訊內容。 視訊章節在視訊清除程式追蹤中顯示為標籤，並在滑鼠滾過或在觸控系統上按一下滑鼠時，顯示章節標題和相關說明。 使用者可以按一下章節標籤或點選章節說明泡泡圖，來尋找特定章節。

檢視器支援Windows裝置上的觸控輸入和滑鼠輸入，且具有觸控式螢幕和滑鼠。 不過，此支援僅限Chrome、Internet Explorer 11和Edge網頁瀏覽器。

此查看器可完全通過鍵盤訪問。

請參閱[鍵盤輔助功能和導航](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 使用視訊檢視器的社交媒體分享工具 {#section-907d316fe1da4b87abb9775f02464704}

視訊檢視器支援社交媒體分享工具。這些工具是使用者介面中的單一按鈕，當使用者點按或點選時，可展開為分享工具列。

共用工具列包含支援之每種共用管道類型的圖示，例如Facebook、Twitter、電子郵件共用、內嵌程式碼共用和連結共用。 啟用電子郵件共用、內嵌共用或連結共用工具時，檢視器會顯示含有對應資料輸入表單的強制回應對話方塊。 呼叫Facebook或Twitter時，檢視器會將使用者重新導向至社交媒體服務的標準共用對話方塊。 共用工具啟動時，也會自動暫停視訊播放。

由於網頁瀏覽器安全性限制，無法以全螢幕模式使用共用工具。

## 內嵌視訊檢視器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同的網頁對檢視者行為有不同的需求。 有時網頁會提供連結，當按一下連結時，就會在個別瀏覽器視窗中開啟檢視器。 在其他情況下，則需直接將檢視器內嵌在托管頁面上。 在後一種情況下，網頁可能具有靜態頁面版面，或使用在不同裝置上或針對不同瀏覽器視窗大小顯示不同的回應式設計。 為了滿足這些需求，檢視器支援三種主要操作模式：快顯視窗、固定大小內嵌和回應式設計內嵌。

平板電腦和行動裝置支援在同一頁內嵌多個影片。 在大多數情況下，一次只能播放一個視訊。 當使用者開始播放一個視訊，然後嘗試播放另一個視訊時，第一個視訊會自動暫停。 自動暫停的視訊會記住目前的播放時間，因此使用者可以隨時回到該視訊並繼續播放。 此規則的唯一例外是Android 4.x裝置上的Chrome瀏覽器，可以同時播放視訊。

**關於快顯模式**

在彈出式模式中，檢視器會在個別的網頁瀏覽器視窗或標籤中開啟。 它會取用整個瀏覽器視窗區域，並在瀏覽器調整大小或裝置方向變更時進行調整。

此模式是行動裝置最常見的模式。 網頁會使用`window.open()` JavaScript呼叫、正確設定的`A` HTML元素或任何其他適當的方法載入檢視器。

建議您對快顯作業模式使用現成可用的HTML頁面。 它稱為[!DNL VideoViewer.html]，位於標準IS-Viewers部署的[!DNL html5/]子資料夾下：

[!DNL <s7viewers_root>/html5/VideoViewer.html]

您可以套用自訂CSS來達到視覺化自訂。

以下是在新視窗中開啟檢視器的HTML程式碼範例：

```
<a href="http://s7d1.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4" target="_blank">Open popup viewer</a>
```

**關於固定大小內嵌模式和回應式內嵌模式**

在內嵌模式中，檢視器會新增至現有網頁，而現有網頁可能已有與檢視器無關的客戶內容。 瀏覽者通常只佔據網頁的一部分房地產。

主要使用案例是以桌上型電腦或平板電腦裝置為導向的網頁，以及可根據裝置類型自動調整版面的回應式設計頁面。

當檢視器在初始載入後未變更大小時，會使用固定大小內嵌。 此選項最適合具有靜態頁面配置的網頁。

回應式設計內嵌假設檢視器可能需要在執行階段中調整大小，以回應其容器`DIV`的大小變更。 最常見的使用案例是將檢視器新增至使用彈性頁面版面的網頁。

在回應式設計內嵌模式中，檢視器的運作方式會因網頁大小其容器`DIV`而有所不同。 如果網頁僅設定容器的寬度`DIV`，保持高度不受限制，則檢視器會根據所使用資產的外觀比例自動選擇其高度。 此方法可確保資產完全符合檢視，而無需在側邊填補。 此使用案例最常用於使用回應式設計配置架構(例如Bootstrap、Foundation等)的網頁。

否則，如果網頁同時設定了查看器容器`DIV`的寬度和高度，則查看器僅填充該區域，並遵循網頁佈局提供的大小。 一個很好的範例是將檢視器內嵌至強制回應覆蓋中，其中覆蓋會根據網頁瀏覽器視窗的大小而調整大小。

**固定大小嵌入**

您可以執行下列操作，將檢視器新增至網頁：

1. 將檢視器JavaScript檔案新增至您的網頁。
1. 定義容器`DIV`。
1. 設定檢視器大小。
1. 建立和初始化檢視器。

1. 將檢視器JavaScript檔案新增至您的網頁。

   建立檢視器需要在HTML標題中新增指令碼標籤。 使用檢視器API之前，請務必加入[!DNL FlyoutViewer.js]。 [!DNL FlyoutViewer.js]檔案位於標準IS-Viewers部署的[!DNL html5/js/]子資料夾下：

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

如果檢視器部署在其中一個AdobeDynamic Media Classic伺服器上，且是從相同網域提供，則可使用相對路徑。 否則，您需指定安裝IS-Viewers之其中一個AdobeDynamic Media Classic伺服器的完整路徑。

相對路徑如下所示：

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/VideoViewer.js"></script>
```

>[!NOTE]
>
>您只應在頁面上參考主要檢視器JavaScript `include`檔案。 您不應在網頁程式碼中參考任何其他JavaScript檔案，而檢視器邏輯可能會在執行階段下載這些檔案。 尤其是，請勿直接參考檢視器從`/s7viewers`內容路徑（稱為統一SDK `include`）載入的HTML5 SDK `Utils.js`程式庫。 原因在於，`Utils.js`或類似的執行階段檢視器程式庫的位置，是由檢視器的邏輯完全管理，且檢視器版本之間的位置變更。 Adobe不會在伺服器上保留舊版次要檢視器`includes`。
>
>
>因此，將檢視器使用的任何次要JavaScript `include`的直接參考放在頁面上，會在未來部署新產品版本時中斷檢視器的功能。

1. 定義容器DIV。

   將空白的DIV元素新增至您希望檢視器顯示的頁面。 DIV元素必須定義其ID，因為此ID稍後會傳遞至檢視器API。 DIV的大小是透過CSS指定。

   預留位置DIV是已定位的元素，這表示`position` CSS屬性已設為`relative`或`absolute`。

   確保全螢幕功能在Internet Explorer中正常運作。 確認DOM中沒有其他元素的堆疊順序比預留位置DIV高。

   以下是定義預留位置DIV元素的範例：

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. 設定檢視器大小

   您可以為檢視器設定靜態大小，方法是以絕對單位為`.s7videoviewer`頂層CSS類別聲明，或使用修飾詞`stagesize`。

   CSS中的大小可以直接放在HTML頁面上，或放在自訂檢視器CSS檔案中，該檔案稍後會指派給Dynamic Media Classic中的檢視器預設集記錄，或使用style命令明確傳遞。

   如需使用CSS來設定檢視器樣式的詳細資訊，請參閱[自訂視訊檢視器](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e)。

   以下是在HTML頁面中定義靜態檢視器大小的範例：

   ```
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   您可以在Dynamic Media Classic的檢視器預設集記錄中設定`stagesize`修飾元，或以`params`集合的檢視器初始化程式碼明確傳遞，或以命令參考區段所述之API呼叫的形式傳遞，如下所示：

   ```
   videoViewer.setParam("stagesize", "640,480");
   ```

   建議使用CSS型方法，此範例中會使用。

1. 建立和初始化檢視器。

   完成上述步驟後，可以建立一個`s7viewers.VideoViewer`類的實例，將所有配置資訊傳遞到其建構子，並在查看器實例上調用`init()`方法。 設定資訊會以JSON物件的形式傳遞至建構函式。 此物件至少應有`containerId`欄位，該欄位包含檢視器容器ID的名稱，並巢狀`params` JSON物件，以及檢視器支援的設定參數。 在此情況下，`params`物件至少必須具有以`serverUrl`屬性傳遞的影像伺服URL、以`videoserverurl`屬性傳遞的視訊伺服器URL，以及以`asset`參數傳遞的初始資產。 JSON型初始化API可讓您使用一行程式碼來建立和啟動檢視器。

   請務必將檢視器容器新增至DOM，讓檢視器程式碼可以透過其ID來尋找容器元素。 有些瀏覽器會延遲建立DOM，直到網頁結尾為止。 如需最大相容性，請在結尾的`BODY`標籤前，或在內文`onload()`事件上呼叫`init()`方法。

   同時，容器元素還不一定是網頁版面的一部分。 例如，可使用指派給它的`display:none`樣式來隱藏它。 在此情況下，檢視器會延遲其初始化程式，直到網頁將容器元素帶回版面的那一刻為止。 發生此情況時，檢視器載入會自動恢復。

   以下是建立查看器實例、將最小必要配置選項傳遞給建構子並調用`init()`方法的示例。 此範例假設`videoViewer`是檢視器例項， `s7viewer`是預留位置`DIV`的名稱， [!DNL http://s7d1.scene7.com/is/image/]是影像伺服URL, [!DNL http://s7d1.scene7.com/is/content/]是視訊伺服器URL，而[!DNL Scene7SharedAssets/Glacier_Climber_MP4]是資產。

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

   以下程式碼是內嵌固定大小視訊檢視器的簡單網頁的完整範例：

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

**無限制高度的回應式設計內嵌**

透過回應式設計內嵌，網頁通常會有某種彈性的版面配置，指定檢視器容器`DIV`的執行時間大小。 在此範例中，假設網頁允許檢視器的容器`DIV`取用40%的網頁瀏覽器視窗大小，使其高度不受限制。 網頁HTML程式碼如下所示：

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

將檢視器新增至此類頁面，與固定大小的內嵌非常類似；唯一的差異是您不需要明確定義檢視器大小。

1. 將檢視器JavaScript檔案新增至您的網頁。
1. 定義容器DIV。
1. 建立和初始化檢視器。

上述所有步驟與固定大小嵌入相同。 將容器`DIV`添加到現有的「保持器」 `DIV`。 下列程式碼為完整的範例。 您可以查看瀏覽器調整大小時檢視器大小的變更，以及檢視器外觀比例與資產的相符情形。

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

下列範例頁面說明在實際中更多使用高度不受限制的回應式設計內嵌：

[即時演示](https://landing.adobe.com/tw/na/dynamic-media/ctir-2755/live-demos.html)

[替代演示位置](https://experienceleague.adobe.com/tools/vlist/vlist.html)

**定義寬度和高度的回應式設計內嵌**

當定義了寬度和高度的回應式設計內嵌時，網頁樣式會有所不同；它會提供「holder」 `DIV`的兩種大小，並將其置於瀏覽器視窗中。 此外，網頁還將`HTML`和`BODY`元素的大小設定為100%:

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

其餘的嵌入步驟與高度不受限制的響應式設計嵌入相同。 產生的範例如下：

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

**使用基於Setter的API嵌入**

您可以使用setter型API和無目標建構函式，而不使用JSON型初始化。 使用該API時，建構函式不會採用任何參數，且會使用具有個別JavaScript呼叫的`setContainerId()`、`setParam()`及`setAsset()` API方法來指定設定參數。

以下示例說明了使用基於setter的API進行固定大小嵌入：

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
