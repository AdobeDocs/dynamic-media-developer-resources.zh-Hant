---
description: HTML5 Video360檢視器是360度的視訊播放器，會播放以H.264格式編碼的串流和漸進式360視訊，由Dynamic Media Classic或AEM Dynamic Media傳送。
solution: Experience Manager
title: Video360
feature: Dynamic Media Classic，檢視器，SDK/API,360 VR影片
role: Developer,User
exl-id: 74dca3f6-ce89-4c5b-8459-c2c4ca8ed27c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '2590'
ht-degree: 0%

---

# Video360{#video}

HTML5 Video360檢視器是360度的視訊播放器，會播放以H.264格式編碼的串流和漸進式360視訊，由Dynamic Media Classic或AEM Dynamic Media傳送。

360度的視頻，又稱為沈浸式視頻或球形視頻，是一些視頻錄像，在這些錄像中，各個方向的觀點同時被記錄下來，使用全向攝像機或一組攝像機拍攝。 支援單一視訊和最適化視訊集。 檢視器另外支援使用裝載於外部位置的漸進式視訊和HLS資料流。

360視訊的建議外觀比例為2:1。 不支援空間音效。 觀看者的設計僅能搭配360部影片使用；嘗試播放非360視訊會導致視訊播放失真。

檢視器的設計可同時在支援HTML5視訊的案頭和行動網頁瀏覽器上運作。 檢視器支援選用的社交分享工具。

每當基礎系統支援HLS格式時，Video360檢視器都會在其預設設定中使用HTML5串流視訊播放。 在不支援HTML5串流的系統上，檢視器會回復為HTML5漸進式視訊傳送。

檢視器類型為517。

## 示範URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS](https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS)

## 系統要求 {#section-b7270cc4290043399681dc504f043609}

請參閱[系統要求](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

## 使用Video360查看器 {#section-e6c68406ecdc4de781df182bbd8088b4}

HTML5視訊360檢視器代表主要的JavaScript檔案和一組協助檔案（單一JavaScript包含此特定檢視器、資產、CSS所使用的所有HTML5檢視器SDK元件），由檢視器在執行階段下載。

HTML5視訊360檢視器可使用隨IS檢視器提供的生產就緒HTML頁面，或在內嵌模式中使用，透過記錄的API整合至目標網頁。

設定和外觀設定與本指南所述其他檢視器的設定和外觀類似。 所有外觀設定都是透過自訂(CSS)階層式樣式表來達成。

請參閱所有檢視器通用的[命令參考 — 設定屬性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)和所有檢視器通用的[命令參考 — URL](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-cmdref-url/c-html5-aem-video360-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

360視訊內容需要比標準非360視訊更高的編碼設定。 換句話說，360個內容的解析度必須高於非360個視頻，才能達到相同的可感知質量。 建議您針對360視訊考慮下列最適化視訊預設集設定：

* 720p,2500 kbps
* 1080p,5000 kbps
* 1440p,6600 kbps

但請注意，使用如此高品質的設定來提供編碼的視訊，需要在一般使用者裝置上提供高頻寬連線。

## 與Video360檢視器互動 {#section-642e66ca38cd4032992840ec6c0b0cd2}

HTML5 Video360 Viewer提供一組用於視訊播放的標準使用者介面控制項，例如播放/暫停按鈕、視訊清除程式視訊時間泡泡、播放時間/總時間指標、音量控制和全螢幕按鈕。 所有這些控制項都會分組到檢視器使用者介面最下方的控制列中。

請注意，在觸摸設備上，音量控制是從用戶介面隱藏的，因為只能使用設備的硬體按鈕控制音量。

檢視器在快顯模式中運作時，使用者介面中無法使用全螢幕按鈕。

檢視器也支援各種社交媒體分享工具。 使用者按一下或點選使用者介面中的單一按鈕，即可展開至共用工具列。 共用工具列包含支援之每種共用管道類型的圖示，例如Facebook、Twitter、電子郵件共用、內嵌程式碼共用和連結共用。 啟用電子郵件共用、內嵌共用或連結共用工具時，檢視器會顯示含有對應資料輸入表單的強制回應對話方塊。 呼叫Facebook或Twitter時，檢視器會將使用者重新導向至社交媒體服務的標準共用對話方塊。 此外，共用工具啟動時，視訊播放會自動暫停。 由於網頁瀏覽器安全性限制，無法以全螢幕模式使用共用工具。

觀看者可在VR頭戴式視頻（如Oculus Go和Oculus Rift）、VR HMD（頭戴式顯示器）安裝（如Google Cardboard）和非VR啟用的設備（如案頭瀏覽器、平板電腦和未連接到VR HMD安裝的行動電話）上支援360個視頻播放。

在VR頭戴式裝置上檢視360個視訊內容不需要額外設定。 檢視器會自動偵測是否有VR頭戴式耳機，並在視訊內容上方顯示「VR」按鈕。 啟用此「VR」按鈕會將視訊轉譯切換為VR模式。 檢視器僅支援在支援WebVR的瀏覽器中轉譯VR。

為了使用VR HMD裝載在觀看者的配置中，`Video360Player.vrrender`修飾符必須設定為`1`，這會強制進行立體呈現。

在VR頭戴式視窗和VR HMD安裝時，視點變更會隨著頭戴式耳機移動而發生，而未在VR模式中提供其他播放控制項。

在未啟用VR的裝置上觀看360視訊時，一般使用者可以使用滑鼠、觸控或鍵盤來控制視訊播放和觀看點。

檢視器在具有觸控螢幕和滑鼠的Windows裝置上，可同時支援觸控輸入和滑鼠輸入，但此支援僅限於Chrome、Internet Explorer 11和Edge網頁瀏覽器。

檢視器可完全鍵盤存取。 請參閱[鍵盤輔助功能和導航](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 嵌入Video360查看器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同的網頁對檢視者行為有不同的需求。 有時網頁會提供連結，當按一下連結時，就會在個別瀏覽器視窗中開啟檢視器。 在其他情況下，則需直接將檢視器內嵌在托管頁面上。 在後一種情況下，網頁可能具有靜態頁面版面，或使用在不同裝置上或針對不同瀏覽器視窗大小顯示不同的回應式設計。 為了滿足這些需求，檢視器支援三種主要操作模式：快顯視窗、固定大小內嵌和回應式設計內嵌。

平板電腦和行動裝置支援在同一頁內嵌多個影片。 在大多數情況下，一次只能播放一個視訊。 當使用者開始播放一個視訊，然後嘗試播放另一個視訊時，第一個視訊會自動暫停。 自動暫停的視訊會記住目前的播放時間，因此使用者可以隨時回到該視訊並繼續播放。 此規則的唯一例外是Android 4.x裝置上的Chrome瀏覽器，可以同時播放視訊。

**關於快顯模式**

在彈出式模式中，檢視器會在個別的網頁瀏覽器視窗或標籤中開啟。 它會取用整個瀏覽器視窗區域，並在瀏覽器調整大小或裝置方向變更時進行調整。

此模式是行動裝置最常見的模式。 網頁會使用`window.open()` JavaScript呼叫、正確設定的`A` HTML元素或任何其他適當的方法載入檢視器。

建議您對快顯作業模式使用現成可用的HTML頁面。 它稱為[!DNL Video360Viewer.html]，位於標準IS-Viewers部署的[!DNL html5/]子資料夾下：

[!DNL <s7viewers_root>/html5/Video360Viewer.html]

您可以套用自訂CSS來達到視覺化自訂。

以下是在新視窗中開啟檢視器的HTML程式碼範例：

```
<a href="https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS" target="_blank">Open popup viewer</a>
```

**關於固定大小嵌入模式和響應式設計嵌入模式**

在內嵌模式中，檢視器會新增至現有網頁，而現有網頁可能已有與檢視器無關的客戶內容。 觀看者通常只佔有網頁的一部分房地產。

主要使用案例是以桌上型電腦或平板電腦裝置為導向的網頁，以及可回應的設計頁面，這些頁面會根據裝置類型自動調整版面。

當檢視器在初始載入後未變更大小時，會使用固定大小內嵌。 這是靜態版面的網頁最佳選擇。

回應式設計內嵌假設檢視器可能需要在執行階段調整大小，以回應其容器`DIV`的大小變更。 最常見的使用案例是在使用彈性頁面版面的網頁中新增檢視器。

在回應式設計內嵌模式中，檢視器的運作方式會因網頁大小其容器`DIV`而有所不同。 如果網頁僅設定容器的寬度`DIV`，保持高度不受限制，則檢視器會根據所使用資產的外觀比例自動選擇其高度。 此功能可確保資產完全符合檢視，而無需邊框上的邊框間距。 此使用案例是使用回應式網頁設計配置架構(例如Bootstrap、Foundation等)的網頁中最常見的使用案例。

否則，如果網頁同時設定了查看器容器`DIV`的寬度和高度，則查看器只會填入該區域，並遵循網頁佈局提供的大小。 一個很好的範例是將檢視器嵌入強制回應覆蓋中，其中覆蓋會根據網頁瀏覽器視窗大小來調整大小。

**固定大小嵌入**

您可以執行下列操作，將檢視器新增至網頁：

1. 將檢視器JavaScript檔案新增至您的網頁。
1. 定義容器`DIV`。
1. 設定檢視器大小。
1. 建立和初始化檢視器。

1. 將檢視器JavaScript檔案新增至您的網頁。

   建立檢視器需要在HTML標題中新增指令碼標籤。 使用檢視器API之前，請務必加入[!DNL Video360Viewer.js]。 [!DNL Video360Viewer.js]檔案位於標準IS-Viewers部署的[!DNL html5/js/]子資料夾下：

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js]

如果檢視器部署在其中一個AdobeDynamic Media Classic伺服器上，且是從相同網域提供，則可使用相對路徑。 否則，您需指定安裝IS-Viewers之其中一個AdobeDynamic Media Classic伺服器的完整路徑。

相對路徑如下所示：

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>您只應在頁面上參考主要檢視器JavaScript `include`檔案。 您不應在網頁程式碼中參考任何其他JavaScript檔案，而檢視器邏輯可能會在執行階段下載這些檔案。 尤其是，請勿直接參考檢視器從`/s7viewers`內容路徑（稱為統一SDK `include`）載入的HTML5 SDK `Utils.js`程式庫。 原因在於，`Utils.js`或類似的執行階段檢視器程式庫的位置，是由檢視器的邏輯完全管理，且檢視器版本之間的位置變更。 Adobe不會在伺服器上保留舊版次要檢視器`includes`。
>
>
>因此，將檢視器使用的任何次要JavaScript `include`的直接參考放在頁面上，會在未來部署新產品版本時中斷檢視器的功能。

1. 定義容器`DIV`。

   將空白的`DIV`元素新增至您希望檢視器顯示的頁面。 `DIV`元素必須已定義其ID，因為此ID稍後會傳遞至檢視器API。 DIV的大小是透過CSS指定。

   佔位符`DIV`是定位的元素，這意味著`position` CSS屬性設定為`relative`或`absolute`。

   若要讓全螢幕功能在Internet Explorer中正常運作，請確定DOM中沒有其他元素的堆疊順序比預留位置`DIV`高。

   以下是定義的佔位符`DIV`元素的示例：

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div>
   ```

1. 設定檢視器大小

   您可以為檢視器設定靜態大小，方法是以絕對單位為`.s7video360viewer`頂層CSS類別聲明，或使用`stagesize`修飾詞。

   您可以直接將CSS中的大小調整放在HTML頁面上，或放在自訂檢視器CSS檔案中，該檔案稍後會指派給AEM Assets — 隨選的檢視器預設集記錄，或使用`style`命令明確傳遞。

   如需使用CSS來設定檢視器樣式的詳細資訊，請參閱[自訂Video360檢視器](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0)。

   以下是在HTML頁面中定義靜態檢視器大小的範例：

   ```
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   您可以在AEM Assets的檢視器預設集記錄中設定`stagesize`修飾詞 — 隨選。 或者，您也可以使用`params`集合的檢視器初始化程式碼，或如「命令參考」區段所述以API呼叫的形式明確傳遞，如下所示：

   ```
   video360viewer.setParam("stagesize", "640,640");
   ```

   建議使用CSS型方法，此範例中會使用。

1. 建立和初始化檢視器。

   完成上述步驟後，可以建立一個`s7viewers.Video360Viewer`類的實例，將所有配置資訊傳遞到其建構子，並在查看器實例上調用`init()`方法。 設定資訊會以JSON物件的形式傳遞至建構函式。 此物件至少應有`containerId`欄位，該欄位包含檢視器容器ID的名稱，並巢狀`params` JSON物件，以及檢視器支援的設定參數。

   在此情況下，`params`物件至少必須以`serverUrl`屬性傳遞影像伺服URL，並以`asset`參數傳遞初始資產。 JSON型初始化API可讓您使用單行程式碼、以`videoserverurl`屬性傳遞的視訊伺服器URL、以`asset`參數傳遞的初始資產，以及以`interactivedata`屬性傳遞的互動式資料，來建立和啟動檢視器。 JSON型初始化API可讓您使用一行程式碼來建立和啟動檢視器。

   請務必將檢視器容器新增至DOM，讓檢視器程式碼可以透過其ID來尋找容器元素。 有些瀏覽器會延遲建立DOM，直到網頁結尾為止。 如需最大相容性，請在結尾的`BODY`標籤前，或在內文`onload()`事件上呼叫`init()`方法。

   同時，容器元素還不一定是網頁版面的一部分。 例如，可使用指派給它的`display:none`樣式來隱藏它。 在此情況下，檢視器會延遲其初始化程式，直到網頁將容器元素帶回版面的那一刻為止。 發生此情況時，檢視器載入會自動繼續。

   以下是建立查看器實例的示例，將最小必要配置選項傳遞給建構子並調用`init()`方法。 此範例假設如下：

   * 查看器實例為`video360Viewer`。
   * 佔位符`DIV`的名稱為`s7viewer`。
   * 影像伺服URL為`https://s7d9.scene7.com/is/image`。
   * 視訊伺服器URL為`https://s7d9.scene7.com/is/content`。
   * 資產為`Viewers/space_station_360-AVS`。

   ```
   <script type="text/javascript"> 
   var video360Viewer = new s7viewers.Video360Viewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/space_station_360-AVS", 
    "serverurl":"https://s7d9.scene7.com/is/image/", 
    "videoserverurl":"https://s7d9.scene7.com/is/content/" 
   } 
   }).init(); 
   </script>
   ```

   以下代碼是嵌入Video360查看器的固定大小的普通網頁的完整示例：

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   <script type="text/javascript"> 
   var video360Viewer = new s7viewers.Video360Viewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/space_station_360-AVS", 
    "serverurl":"https://s7d9.scene7.com/is/image/", 
    "videoserverurl":"https://s7d9.scene7.com/is/content/" 
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
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
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
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**定義寬度和高度的回應式內嵌**

若定義了寬度和高度的回應式內嵌，網頁樣式會有所不同。 它會為`"holder"` DIV提供兩種大小，並在瀏覽器視窗中將其置中。 此外，網頁還將`HTML`和`BODY`元素的大小設定為100%。

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
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
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
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
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
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7video360viewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var video360Viewer = new s7viewers.Video360Viewer(); 
video360Viewer.setContainerId("s7viewer"); 
video360Viewer.setParam("serverurl", "https://s7d9.scene7.com/is/image/"); 
video360Viewer.setParam("videoserverurl", "https://s7d9.scene7.com/is/content/"); 
video360Viewer.setAsset("Viewers/space_station_360-AVS"); 
video360Viewer.init(); 
</script> 
</body> 
</html>
```
