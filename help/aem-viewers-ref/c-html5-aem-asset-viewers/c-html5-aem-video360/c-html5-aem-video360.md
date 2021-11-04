---
title: Video360
description: HTML5 Video360檢視器是360度的視訊播放器，播放以H.264格式編碼的串流和漸進式360視訊，由Dynamic Media Classic或Dynamic MediaAdobe Experience Manager傳送。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 74dca3f6-ce89-4c5b-8459-c2c4ca8ed27c
source-git-commit: fd3a1fe47da5ba26b53ea9414bfec1e4c11d7392
workflow-type: tm+mt
source-wordcount: '2569'
ht-degree: 0%

---

# Video360{#video}

HTML5 Video360檢視器是360度的視訊播放器，播放以H.264格式編碼的串流和漸進式360視訊，由Dynamic Media Classic或Dynamic MediaAdobe Experience Manager傳送。

360度的視頻，又稱為沈浸式視頻或球形視頻，是一些視頻錄像，在這些錄像中，各個方向的觀點同時被記錄下來，使用全向攝像機或一組攝像機拍攝。 支援單一視訊和最適化視訊集。 檢視器也支援使用外部位置上托管的漸進式視訊和HLS資料流。

360視訊的建議外觀比例為2:1。 不支援空間音效。 觀看者的設計僅能搭配360部影片使用；嘗試播放非360視訊會導致視訊播放失真。

檢視器的設計可同時在支援HTML5視訊的案頭和行動網頁瀏覽器上運作。 檢視器支援選用的社交分享工具。

每當基礎系統支援HLS格式時，Video360 Viewer都會在其預設配置中使用HLS格式的HTML5串流視訊播放。 在不支援HTML5串流的系統上，檢視器會回復為HTML5漸進式視訊傳送。

檢視器類型為517。

## 示範URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS](https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS)

## 系統要求 {#section-b7270cc4290043399681dc504f043609}

請參閱 [系統需求](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## 使用Video360查看器 {#section-e6c68406ecdc4de781df182bbd8088b4}

HTML5視訊360檢視器代表主要的JavaScript檔案和檢視器在執行階段下載的一組協助檔案(單一JavaScript包含此檢視器、資產、CSS所使用的所有HTML5檢視器SDK元件)。

HTML5視訊360檢視器可使用隨IS檢視器提供的生產就緒HTML頁面，或在內嵌模式中使用，透過記錄的API整合至目標網頁。

設定和外觀與本指南中所述其他檢視器的設定和外觀類似。 所有外觀設定都是透過自訂(CSS)階層式樣式表來達成。

請參閱 [所有檢視器通用的命令參考 — 設定屬性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 和 [所有檢視器 — URL通用的命令參考](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-cmdref-url/c-html5-aem-video360-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

360視訊內容需要比標準非360視訊更高的編碼設定。 換句話說，360個內容的解析度必須高於非360個視頻，才能達到相同的可感知質量。 建議您針對360視訊考慮下列最適化視訊預設集設定：

* 720p,2500 kbps
* 1080p,5000 kbps
* 1440p,6600 kbps

但請注意，使用如此高品質的設定來提供編碼的視訊，需要在一般使用者裝置上進行高頻寬連線。

## 與Video360檢視器互動 {#section-642e66ca38cd4032992840ec6c0b0cd2}

HTML5視訊360檢視器提供一組用於視訊播放的標準使用者介面控制項，例如播放/暫停按鈕、視訊清除程式視訊時間泡泡、播放時間/總時間指標、音量控制和全螢幕按鈕。 所有這些控制項都會分組到檢視器使用者介面底部的控制列中。

在觸摸設備上，音量控制在用戶介面中隱藏，因為只能使用設備的硬體按鈕控制音量。

檢視器在快顯模式中運作時，使用者介面中無法使用全螢幕按鈕。

檢視器也支援各種社交媒體分享工具。 使用者按一下或點選使用者介面中的單一按鈕，即可展開至共用工具列。 共用工具列包含支援之每種共用管道類型的圖示，例如Facebook、Twitter、電子郵件共用、內嵌程式碼共用和連結共用。 啟用電子郵件共用、內嵌共用或連結共用工具時，檢視器會顯示含有對應資料輸入表單的強制回應對話方塊。 呼叫Facebook或Twitter時，檢視器會將使用者重新導向至社交媒體服務的標準共用對話方塊。 此外，共用工具啟動時，視訊播放會自動暫停。 由於網頁瀏覽器安全性限制，無法以全螢幕模式使用共用工具。

檢視器支援下列播放360個視訊：

* VR頭戴式耳機(例如Oculus Go和Oculus Rift)
* VR HMD（頭裝顯示器）安裝(如Google Cardboard)
* 未啟用VR的裝置（例如未連線至VR HMD載入的案頭瀏覽器、平板電腦和行動電話）

在VR頭戴式耳機上檢視360個視訊內容無需額外設定。 檢視器會自動偵測是否有VR頭戴式耳機，並在視訊內容上方顯示「VR」按鈕。 啟用此「VR」按鈕會將視訊轉譯切換為VR模式。 檢視器僅支援在支援WebVR的瀏覽器中轉譯VR。

為了使用VR HMD裝載 `Video360Player.vrrender` 修飾詞必須設定為 `1` 在檢視器的設定中，會強制進行立體呈現。

在VR耳機和VR HMD安裝上，視點變更會隨著頭戴式耳機移動而發生，而不是在VR模式中提供其他播放控制項。

在未啟用VR的裝置上觀看360視訊時，一般使用者可以使用滑鼠、觸控或鍵盤來控制視訊播放和觀看點。

檢視器在具有觸控螢幕和滑鼠的Windows裝置上，可同時支援觸控輸入和滑鼠輸入，但此支援僅限於Chrome、Internet Explorer 11和Edge網頁瀏覽器。

檢視器可完全鍵盤存取。 請參閱 [鍵盤協助工具和導覽](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## 嵌入Video360查看器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同的網頁對檢視者行為有不同的需求。 有時，網頁會提供連結，當選取時，連結會在個別瀏覽器視窗中開啟檢視器。 在其他情況下，則需直接將檢視器內嵌在托管頁面上。 在後一種情況下，網頁可能具有靜態頁面版面，或使用在不同裝置上或針對不同瀏覽器視窗大小顯示不同的回應式設計。 為了滿足這些需求，檢視器支援三種主要操作模式：快顯視窗、固定大小內嵌和回應式設計內嵌。

平板電腦和行動裝置支援在同一頁內嵌多個影片。 通常一次只能播放一個視訊。 當使用者開始播放一個視訊，然後嘗試播放另一個視訊時，第一個視訊會自動暫停。 自動暫停的視訊會記住目前的播放時間，因此使用者可以隨時回到該視訊並繼續播放。 此規則的唯一例外是Android™ 4.x裝置上的Chrome瀏覽器，可同時播放視訊。

**關於快顯模式**

在快顯模式中，檢視器會在個別的網頁瀏覽器視窗或標籤中開啟。 它會取用整個瀏覽器視窗區域，並在瀏覽器調整大小或裝置方向變更時進行調整。

此模式是行動裝置最常見的模式。 網頁會使用 `window.open()` JavaScript呼叫，已正確設定 `A` HTML元素，或任何其他合適的方法。

建議您對快顯操作模式使用現成可用的HTML頁面。 稱為 [!DNL Video360Viewer.html] 位於 [!DNL html5/] 標準IS — 檢視器部署的子資料夾：

[!DNL <s7viewers_root>/html5/Video360Viewer.html]

您可以套用自訂CSS來達到視覺化自訂。

以下是在新視窗中開啟檢視器的HTML程式碼範例：

```
<a href="https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS" target="_blank">Open popup viewer</a>
```

**關於固定大小嵌入模式和響應式設計嵌入模式**

在內嵌模式中，檢視器會新增至現有網頁，而現有網頁可能已有與檢視器無關的客戶內容。 觀看者通常只佔有網頁的一部分房地產。

主要使用案例是以桌上型電腦或平板電腦裝置為導向的網頁，以及可回應的設計頁面，這些頁面會根據裝置類型自動調整版面。

當檢視器在初始載入後未變更大小時，會使用固定大小內嵌。 此方法是靜態版面的網頁最佳選擇。

回應式設計內嵌假設檢視器必須在執行階段調整大小，以回應其容器的大小變更 `DIV`. 最常見的使用案例是在使用彈性頁面版面的網頁中新增檢視器。

在回應式設計內嵌模式中，檢視器的運作方式會因網頁大小其容器的方式而異 `DIV`. 如果網頁僅設定容器的寬度 `DIV`，而不限制其高度，則檢視器會根據所使用資產的外觀比例自動選取高度。 此功能可確保資產完全符合檢視，而無需邊框上的邊框間距。 此使用案例是使用回應式網頁設計配置架構(例如Bootstrap和Foundation)的網頁中最常見的使用案例。

否則，如果網頁同時設定檢視器容器的寬度和高度 `DIV`，則檢視器會填入該區域，並遵循網頁版面提供的大小。 一個很好的範例是將檢視器嵌入強制回應覆蓋中，其中覆蓋會根據網頁瀏覽器視窗大小來調整大小。

**固定大小嵌入**

您可以執行下列操作，將檢視器新增至網頁：

1. 將檢視器JavaScript檔案新增至您的網頁。
1. 定義容器 `DIV`.
1. 設定檢視器大小。
1. 建立和初始化檢視器。

1. 將檢視器JavaScript檔案新增至您的網頁。

   建立檢視器需要在HTML標題中新增指令碼標籤。 使用檢視器API之前，請務必加入 [!DNL Video360Viewer.js]. 此 [!DNL Video360Viewer.js] 檔案位於 [!DNL html5/js/] 標準IS — 檢視器部署的子資料夾：

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js]

如果檢視器部署在其中一個Adobe Dynamic Media Classic伺服器上，且是從相同網域提供，則可使用相對路徑。 否則，您會指定安裝IS-Viewers之一Adobe Dynamic Media Classic伺服器的完整路徑。

相對路徑如下所示：

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>僅參考主要檢視器JavaScript `include` 檔案。 請勿在網頁程式碼中參考任何其他JavaScript檔案，這些檔案可能會由檢視器的邏輯在執行階段下載。 尤其是，請勿直接參考HTML5 SDK `Utils.js` 檢視器從 `/s7viewers` 內容路徑（所謂的整合SDK） `include`)。 原因是 `Utils.js` 或者，檢視器的邏輯和檢視器版本之間的位置變更，可完全管理類似的執行階段檢視器程式庫。 Adobe不會保留舊版次要檢視器 `includes` 在伺服器上。
>
>
>因此，請直接參考任何次要JavaScript `include` 若將來部署新產品版本，則檢視器在頁面上使用時會中斷檢視器功能。

1. 定義容器 `DIV`.

   新增空白 `DIV` 元素，以顯示檢視器的頁面。 此 `DIV` 元素必須已定義其ID，因為此ID稍後會傳遞至檢視器API。 DIV的大小是透過CSS指定。

   預留位置 `DIV` 是定位的元素，表示 `position` CSS屬性設為 `relative` 或 `absolute`.

   若要讓全螢幕功能在Internet Explorer中正常運作，請確定DOM中沒有其他元素的堆疊順序比預留位置高 `DIV`.

   以下是定義預留位置的範例 `DIV` 元素：

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div>
   ```

1. 設定檢視器大小

   您可以為聲明來設定檢視器的靜態大小 `.s7video360viewer` 頂層CSS類（以絕對單位表示），或使用 `stagesize` 修飾詞。

   您可以直接將CSS中的大小調整放在HTML頁面上，或放在自訂檢視器CSS檔案中，該檔案稍後會指派給Adobe Experience Manager Assets - On-demand中的檢視器預設集記錄，或使用明確傳遞 `style` 命令。

   請參閱 [自定義Video360查看器](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) 以取得有關使用CSS來設定檢視器樣式的詳細資訊。

   以下是在「HTML」頁面中定義靜態檢視器大小的範例：

   ```
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   您可以設定 `stagesize` AEM Assets中檢視器預設集記錄中的修飾元 — 隨選。 或者，您也可以使用檢視器初始化程式碼，以明確的方式傳遞 `params` 集合，或以API呼叫的形式（如命令參考區段所述），如下所示：

   ```
   video360viewer.setParam("stagesize", "640,640");
   ```

   建議使用CSS型方法，此範例中會使用。

1. 建立和初始化檢視器。

   完成上述步驟後，請建立例項 `s7viewers.Video360Viewer` 類，將所有配置資訊傳遞到其建構子，並調用 `init()` 方法。 設定資訊會以JSON物件的形式傳遞至建構函式。 至少，此物件應具有 `containerId` 欄位，其中包含檢視器容器ID的名稱和巢狀 `params` 檢視器支援之設定參數的JSON物件。

   在此情況下， `params` 物件至少必須以 `serverUrl` 屬性，而初始資產為 `asset` 參數。 JSON型初始化API可讓您使用一行程式碼(視訊伺服器URL，以 `videoserverurl` 屬性，初始資產為 `asset` 參數和互動式資料 `interactivedata` 屬性。 JSON型初始化API可讓您使用一行程式碼來建立和啟動檢視器。

   請務必將檢視器容器新增至DOM，讓檢視器程式碼可以透過其ID來尋找容器元素。 有些瀏覽器會延遲建立DOM，直到網頁結尾為止。 如需最大相容性，請呼叫 `init()` 方法 `BODY` 標籤，或在內文上 `onload()` 事件。

   同時，容器元素還不一定是網頁版面的一部分。 例如，您可能會使用 `display:none` 樣式。 在此情況下，檢視器會延遲其初始化程式，直到網頁將容器元素帶回版面的那一刻為止。 發生此情況時，檢視器載入會自動繼續。

   以下是建立檢視器例項的範例，將最低必要的設定選項傳遞至建構函式，並呼叫 `init()` 方法。 此範例假設如下：

   * 檢視器例項為 `video360Viewer`.
   * 佔位符的名稱 `DIV` is `s7viewer`.
   * 影像提供URL為 `https://s7d9.scene7.com/is/image`.
   * 視訊伺服器URL為 `https://s7d9.scene7.com/is/content`.
   * 資產為 `Viewers/space_station_360-AVS`.

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

透過回應式設計內嵌，網頁通常會有某種彈性的版面配置，而這會決定檢視器容器的執行階段大小 `DIV`. 在下列範例中，假設網頁允許檢視器的容器 `DIV` 取用40%的網頁瀏覽器視窗大小，使其高度不受限制。 網頁HTML程式碼如下所示：

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

上述所有步驟與固定大小嵌入相同。 將容器DIV新增至現有 `"holder"` DIV. 下列程式碼為完整的範例。 注意當瀏覽器調整大小時，檢視器大小會如何變更，以及檢視器外觀比例與資產如何相符。

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

如果定義了寬度和高度的回應式內嵌，則網頁樣式會不同。 它為 `"holder"` DIV並在瀏覽器視窗中將其置中。 此外，網頁會設定 `HTML` 和 `BODY` 100%。

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

您可以使用setter型API和無目標建構函式，而不使用JSON型初始化。 使用此API建構函式不會取用任何參數，且會使用 `setContainerId()`, `setParam()`，和 `setAsset()` API方法搭配個別的JavaScript呼叫。

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
