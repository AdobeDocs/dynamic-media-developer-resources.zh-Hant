---
title: Video360
description: HTML5 Video360 Viewer是一種360度影片播放程式，可播放從Dynamic Media Classic或Adobe Experience Manager、Dynamic Media傳送的H.264格式串流及漸進式360影片。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 74dca3f6-ce89-4c5b-8459-c2c4ca8ed27c
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2568'
ht-degree: 0%

---

# Video360{#video}

HTML5 Video360 Viewer是一種360度影片播放程式，可播放從Dynamic Media Classic或Adobe Experience Manager、Dynamic Media傳送的H.264格式串流及漸進式360影片。

360度影片（也稱為沈浸式影片或球形影片）是同時錄製每個方向的檢視的影片，使用全方位相機或相機集合拍攝。 同時支援單一視訊和自我調整視訊集。 此檢視器也支援使用託管於外部位置的漸進式視訊和HLS資料流。

360度視訊的建議外觀比例為2:1。 不支援空間音效。 檢視器的設計僅能處理360度視訊；嘗試播放非360度視訊會導致視訊播放失真。

此檢視器的設計可在支援HTML5視訊的案頭和行動網頁瀏覽器上運作。 檢視器支援選用的社交分享工具。

只要基礎系統支援，Video360 Viewer就會在其預設設定中使用HLS格式的HTML5串流視訊播放。 在不支援HTML5串流的系統上，檢視器會回到HTML5漸進式視訊傳送。

檢視器型別為517。

## 示範URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS](https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS)

## 系統要求 {#section-b7270cc4290043399681dc504f043609}

另請參閱 [系統需求](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## 使用Video360檢視器 {#section-e6c68406ecdc4de781df182bbd8088b4}

HTML5 Video360檢視器代表檢視器在執行階段下載的主要JavaScript檔案和一組協助程式檔案(單一JavaScript包含此檢視器使用的所有HTML5 Viewer SDK元件、資產、CSS)。

HTML5 Video360 Viewer既可透過隨IS-Viewers提供的生產就緒HTML頁面以快顯視窗模式使用，也可透過內嵌模式使用，透過已記錄的API整合至目標網頁。

組態和外觀設定類似於本指南中描述的其他檢視器。 所有外觀設定都是透過自訂(CSS)階層式樣式表來達成。

另請參閱 [所有檢視器通用的命令參考 — 組態屬性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 和 [所有檢視器通用的命令參考 — URL](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-cmdref-url/c-html5-aem-video360-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

360度影片內容需要的編碼設定比標準的非360度影片更高。 換句話說，360內容必須比非360影片具有更高的解析度，才能達到相同的視覺品質。 建議您針對360度影片考慮下列最適化影片預設集設定：

* 720p， 2500 kbps
* 1080p， 5000 kbps
* 1440p， 6600 kbps

但是請注意，提供使用這類高品質設定編碼的視訊需要一般使用者裝置上的高頻寬連線。

## 與Video360檢視器互動 {#section-642e66ca38cd4032992840ec6c0b0cd2}

HTML5 Video360 Viewer提供一組標準使用者介面控制項供視訊播放使用，例如播放/暫停按鈕、視訊筆畫壓感視訊時間泡泡、播放時間/總時間指標、音量控制項及全熒幕按鈕。 所有這些控制項都會分組到檢視器使用者介面底部的控制項列中。

在觸控裝置上，音量控制會隱藏在使用者介面中，因為只能使用裝置的硬體按鈕來控制音量。

當檢視器在快顯視窗模式下操作時，全熒幕按鈕在使用者介面中無法使用。

檢視器也支援各種社群媒體分享工具。 它們可作為使用者介面中的單一按鈕使用，當使用者按一下或點選共用工具列時，該按鈕會展開至共用工具列。 共用工具列包含每個支援共用管道型別的圖示，例如Facebook、Twitter、電子郵件共用、內嵌程式碼共用和連結共用。 啟動電子郵件共用、內嵌共用或連結共用工具時，檢視器會顯示模型對話方塊，其中包含對應的資料輸入表單。 呼叫Facebook或Twitter時，檢視器會將使用者從社群媒體服務重新導向至標準共用對話方塊。 此外，當共用工具啟動時，視訊播放會自動暫停。 因為Web瀏覽器安全限制，所以無法在全熒幕模式中使用共用工具。

檢視器支援以下專案的360度視訊播放：

* VR耳機(例如Oculus Go和Oculus Rift)
* VR HMD （頭戴式顯示器）掛載(如Google Cardboard)
* 非VR裝置（例如桌上型瀏覽器、平板電腦及未連線至VR HMD掛載的行動電話）

在VR頭戴式耳機上檢視360視訊內容無需額外設定。 檢視器會自動偵測是否有VR頭戴式耳機，並在視訊內容上方顯示「VR」按鈕。 啟用此「VR」按鈕會將視訊演算切換至VR模式。 此檢視器僅在支援WebVR的瀏覽器中支援VR演算。

若要使用VR HMD，請安裝 `Video360Player.vrrender` 修飾元必須設為 `1` 在檢視器的設定中強制進行立體轉譯。

在VR頭戴式耳機和VR HMD掛載上，視點會因應頭戴式耳機的移動而改變，而不是在VR模式中提供其他播放控制。

在非VR裝置上觀看360度影片時，一般使用者可使用滑鼠、觸控或鍵盤來控制影片播放和檢視點。

該檢視器在具有觸控熒幕和滑鼠的Windows裝置上支援觸控輸入和滑鼠輸入，但是這項支援僅限Chrome、Internet Explorer 11和Edge網頁瀏覽器。

檢視器可使用完整的鍵盤。 另請參閱 [鍵盤協助工具和導覽](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## 內嵌Video360檢視器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同的網頁對檢視者的行為有不同的需求。 有時，網頁會提供連結，在選取時會在個別瀏覽器視窗中開啟檢視器。 在其他情況下，需要直接將檢視器內嵌在託管頁面上。 在後一種情況下，網頁可能會有靜態頁面佈局，或使用在不同裝置上或不同瀏覽器視窗大小下顯示不同的回應式設計。 為了滿足這些需求，檢視器支援三種主要操作模式：快顯視窗、固定大小嵌入和回應式設計嵌入。

平板電腦和行動裝置支援在同一頁面上內嵌多個影片。 通常一次只能播放一個視訊。 當使用者開始播放一個影片，然後嘗試播放另一個影片時，會自動暫停第一個影片。 自動暫停的視訊會記住其目前的播放時間，因此使用者可以隨時返回視訊並繼續播放。 此規則唯一的例外是Android™ 4.x裝置上的Chrome瀏覽器，該瀏覽器可同時播放視訊。

**關於彈出式模式**

在快顯視窗模式中，檢視器會在個別的網頁瀏覽器視窗或標籤中開啟。 它會取用整個瀏覽器視窗區域，並在瀏覽器調整大小或裝置方向變更時進行調整。

此模式在行動裝置中最常見。 網頁會使用載入檢視器 `window.open()` javascript呼叫，已正確設定 `A` HTML元素或任何其他適當的方法。

建議您為快顯視窗操作模式使用現成的HTML頁面。 其名稱為 [!DNL Video360Viewer.html] 而且它位於 [!DNL html5/] 標準IS-Viewers部署的子資料夾：

[!DNL <s7viewers_root>/html5/Video360Viewer.html]

您可以套用自訂CSS以實現視覺化自訂。

以下是在新視窗中開啟檢視器的HTML程式碼範例：

```html {.line-numbers}
<a href="https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS" target="_blank">Open popup viewer</a>
```

**關於固定大小內嵌模式和回應式設計內嵌模式**

在內嵌模式中，檢視器會新增至現有網頁，其中可能已有某些與檢視器無關的客戶內容。 檢視器通常只會佔用網頁的一部分空間。

主要使用案例是針對桌上型電腦或平板電腦裝置的網頁，以及可依據裝置型別自動調整版面的回應式設計頁面。

當檢視器在初始載入後未變更其大小時，會使用固定大小內嵌。 此方法適用於具有靜態配置的網頁。

回應式設計內嵌假設檢視器必須在執行階段調整大小以回應容器大小變更 `DIV`. 最常見的使用案例是將檢視器新增到使用彈性頁面配置的網頁。

在回應式設計內嵌模式中，檢視器的行為會因網頁大小其容器的方式而異 `DIV`. 如果網頁僅設定容器的寬度 `DIV`，只要其高度不受限制，檢視器就會根據所使用資產的外觀比例，自動選擇高度。 此功能可確保資產完全符合檢視方式，且兩側不會有任何邊框間距。 此使用案例最常用於使用回應式網頁設計配置架構(例如Bootstrap和Foundation)的網頁。

否則，如果網頁同時設定檢視器容器的寬度和高度 `DIV`，檢視器會填滿該區域，並遵循網頁版面提供的大小。 一個好的範例是內嵌檢視器至強制回應覆蓋圖，其中覆蓋圖會根據網頁瀏覽器視窗大小而調整。

**固定大小內嵌**

您可以執行下列動作，將檢視器新增至網頁：

1. 正在將檢視器JavaScript檔案新增至您的網頁。
1. 定義容器 `DIV`.
1. 設定檢視器大小。
1. 正在建立和初始化檢視器。

1. 正在將檢視器JavaScript檔案新增至您的網頁。

   建立檢視器需要您在HTML標題中新增指令碼標籤。 在可以使用檢視器API之前，請務必加入 [!DNL Video360Viewer.js]. 此 [!DNL Video360Viewer.js] 檔案位於 [!DNL html5/js/] 標準IS-Viewers部署的子資料夾：

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js]

如果檢視器部署在任一Adobe Dynamic Media Classic伺服器上，且從相同網域提供服務，您就可以使用相對路徑。 否則，請指定已安裝IS-Viewers之其中一個Adobe Dynamic Media Classic伺服器的完整路徑。

相對路徑如下所示：

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>僅參照主要檢視器JavaScript `include` 檔案時，才會追蹤此專案。 請勿在網頁程式碼中參考任何其他JavaScript檔案（這些檔案可能由檢視器的邏輯在執行階段下載）。 尤其請勿直接參照HTML5 SDK `Utils.js` 檢視器從載入的程式庫 `/s7viewers` 內容路徑（所謂整合SDK） `include`)。 原因在於 `Utils.js` 或類似的執行階段檢視器程式庫完全由檢視器的邏輯管理，且位置會在檢視器發行版本之間變更。 Adobe不會保留舊版的次要檢視器 `includes` 在伺服器上。
>
>
>因此，直接參照任何次要JavaScript `include` 日後當部署新產品版本時，頁面上檢視器使用的檢視器功能會中斷檢視器。

1. 定義容器 `DIV`.

   新增空白 `DIV` 元素新增至要顯示檢視器的頁面。 此 `DIV` 元素必須定義其ID，因為此ID稍後會傳遞至檢視器API。 DIV的大小是透過CSS指定。

   預留位置 `DIV` 是定位元素，表示 `position` CSS屬性已設定為 `relative` 或 `absolute`.

   為了讓全熒幕功能在Internet Explorer中正常運作，請確定DOM中沒有其他元素的棧疊順序高於預留位置 `DIV`.

   以下為已定義預留位置的範例 `DIV` 元素：

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div>
   ```

1. 設定檢視器大小

   您可以宣告檢視器的靜態大小 `.s7video360viewer` 頂層CSS類別（以絕對單位表示），或使用 `stagesize` 修飾元。

   您可以將CSS的大小直接放在HTML頁面上，或放在自訂檢視器CSS檔案中(稍後會在Adobe Experience Manager Assets中指派給檢視器預設集記錄 — 隨選)，或透過以下方式明確傳遞： `style` 命令。

   另請參閱 [自訂Video360檢視器](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) 以取得有關使用CSS設定檢視器樣式的詳細資訊。

   以下是在「HTML」頁面中定義靜態檢視器大小的範例：

   ```html {.line-numbers}
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   您可以設定 `stagesize` AEM Assets中檢視器預設集記錄的修飾元 — 隨選。 或者，您可以使用檢視器初始化程式碼明確傳遞 `params` 集合，或作為API呼叫，如命令參考區段所述，如下所示：

   ```html {.line-numbers}
   video360viewer.setParam("stagesize", "640,640");
   ```

   此範例建議您使用以CSS為基礎的方法。

1. 正在建立和初始化檢視器。

   完成上述步驟後，您會建立 `s7viewers.Video360Viewer` 類別，將所有設定資訊傳遞至其建構函式，並呼叫 `init()` 方法。 組態資訊會以JSON物件的形式傳遞至建構函式。 此物件至少應具有 `containerId` 包含檢視器容器ID名稱且以巢狀顯示的欄位 `params` 具有檢視器支援之設定引數的JSON物件。

   在此案例中， `params` 物件必須至少將「影像伺服」URL傳遞為 `serverUrl` 屬性，並將初始資產設為 `asset` 引數。 JSON型初始化API可讓您透過以下傳遞的一行程式碼來建立及啟動檢視器：視訊伺服器URL `videoserverurl` 屬性，初始資產為 `asset` 引數，互動式資料為 `interactivedata` 屬性。 JSON型初始化API可讓您使用一行程式碼來建立和啟動檢視器。

   請務必將檢視器容器新增至DOM，讓檢視器程式碼可依其ID尋找容器元素。 有些瀏覽器會延遲建立DOM，直到網頁結尾為止。 如需最大相容性，請呼叫 `init()` 方法（在結尾之前） `BODY` 標籤上，或在內文上 `onload()` 事件。

   同時，容器元素也不一定屬於網頁版面配置的一部分。 例如，可使用以下專案將其隱藏： `display:none` 樣式已指派給它。 在此情況下，檢視器會延遲其初始化程式，直到網頁將容器元素帶回版面配置為止。 發生此情況時，檢視器會自動繼續載入。

   以下範例說明如何建立檢視器例項、將最低必要的設定選項傳遞至建構函式，以及呼叫 `init()` 方法。 此範例假設以下情況：

   * 檢視器例項為 `video360Viewer`.
   * 預留位置名稱 `DIV` 是 `s7viewer`.
   * 「影像伺服」URL為 `https://s7d9.scene7.com/is/image`.
   * 視訊伺服器URL為 `https://s7d9.scene7.com/is/content`.
   * 資產是 `Viewers/space_station_360-AVS`.

   ```html {.line-numbers}
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

   下列程式碼是嵌入固定大小Video360檢視器的簡單網頁的完整範例：

   ```html {.line-numbers}
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

**高度不受限制的回應式設計內嵌**

透過回應式設計內嵌，網頁通常會有某種彈性的版面配置，可指定檢視器容器的執行階段大小 `DIV`. 對於以下範例，假設網頁允許檢視器的容器 `DIV` 佔用40%的網頁瀏覽器視窗大小，其高度不受限制。 網頁HTML程式碼如下所示：

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

1. 正在將檢視器JavaScript檔案新增至您的網頁。
1. 定義容器DIV。
1. 正在建立和初始化檢視器。

上述所有步驟與內嵌固定大小相同。 將容器DIV新增至現有的 `"holder"` DIV. 下列程式碼為完整的範例。 請注意瀏覽器調整大小時檢視器大小的變化，以及檢視器外觀比例與資產的相符情形。

```html {.line-numbers}
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

如果有已定義寬度和高度的回應式內嵌，則網頁樣式會不同。 它提供兩種大小給 `"holder"` 在瀏覽器視窗中進行DIV和置中。 此外，網頁會設定 `HTML` 和 `BODY` 元素至100%。

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

**使用Setter型API進行內嵌**

除了使用JSON型初始化之外，也可以使用setter型API和no-args建構函式。 使用此API建構函式不接受任何引數，而且設定引數是使用 `setContainerId()`， `setParam()`、和 `setAsset()` API方法與個別的JavaScript呼叫。

下列範例說明如何將固定大小內嵌與setter型API搭配使用：

```html {.line-numbers}
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
