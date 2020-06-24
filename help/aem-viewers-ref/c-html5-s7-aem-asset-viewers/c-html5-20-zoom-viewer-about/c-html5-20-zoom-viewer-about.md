---
description: 縮放檢視器是可顯示縮放影像的影像檢視器。 此檢視器可處理影像集，並使用色票進行導覽。 它提供縮放工具、全螢幕支援、色票和選購的關閉按鈕。 它可在桌上型電腦和行動裝置上運作。
keywords: responsive
seo-description: 縮放檢視器是可顯示縮放影像的影像檢視器。 此檢視器可處理影像集，並使用色票進行導覽。 它提供縮放工具、全螢幕支援、色票和選購的關閉按鈕。 它可在桌上型電腦和行動裝置上運作。
seo-title: Zoom
solution: Experience Manager
title: Zoom
topic: Dynamic media
uuid: ec2a91e2-ce2c-48b1-a2b2-8671524288c7
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '2460'
ht-degree: 0%

---


# 縮放{#zoom}

縮放檢視器是可顯示縮放影像的影像檢視器。 此檢視器可處理影像集，並使用色票進行導覽。 它提供縮放工具、全螢幕支援、色票和選購的關閉按鈕。 它可在桌上型電腦和行動裝置上運作。

>[!NOTE]
>
>此檢視器不支援使用IR（影像演算）或UGC（使用者產生的內容）的影像。

檢視器類型502。

請參 [閱系統需求和先決條件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

## 示範URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## 使用縮放檢視器 {#section-e6c68406ecdc4de781df182bbd8088b4}

縮放檢視器代表主要JavaScript檔案和一組輔助檔案（單一JavaScript包含此特定檢視器使用的所有檢視器SDK元件、資產、CSS），由檢視器在執行時期下載。

您可以使用隨IS檢視器提供的可立即生產使用的HTML頁面，或在內嵌模式下，在快顯模式下使用縮放檢視器，在內嵌模式下，使用檔案化的API將縮放檢視器整合至目標網頁。

設定和外觀設定與其他檢視器類似。 所有外觀設定都是透過自訂CSS來完成。

請參 [閱所有檢視器通用的命令參考——所有檢視器通用的組態屬性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)[和命令參考- URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 與縮放檢視器互動 {#section-642e66ca38cd4032992840ec6c0b0cd2}

縮放檢視器支援下列觸控手勢，這些手勢在其他行動應用程式中很常見。 當檢視器無法處理使用者的滑動手勢時，會將事件轉送至網頁瀏覽器，以執行原生頁面捲動。 即使檢視器佔據大部分裝置螢幕區域，這類功能仍可讓使用者瀏覽整個頁面。

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>手勢 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>單鍵 </p> </td> 
   <td colname="col2"> <p> 在色票中選取新的縮圖。 在主檢視中，它會隱藏或揭示使用者介面元素。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>按兩下 </p> </td> 
   <td colname="col2"> <p> 放大一個層級，直到達到放大率上限。 下一個點選手勢會將檢視器重設為初始檢視狀態。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>夾捏 </p> </td> 
   <td colname="col2"> <p>放大或縮小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>水準滑動或輕拂 </p> </td> 
   <td colname="col2"> <p> 在色票列中的色票清單中捲動。 </p> <p> 如果影像處於重設狀態，且 <span class="codeph"> frametransition參 </span> 數設定為滑動，則會使用投影片動畫變更資產。 對於其他 <span class="codeph"> 幀轉 </span> 換模式，手勢會執行原生頁面滾動。 </p> <p> 如果影像放大，則會水準移動影像。 如果影像移至檢視邊緣，並以相同方向執行滑動，則手勢會執行原生頁面捲動。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直滑動 </p> </td> 
   <td colname="col2"> <p> 如果影像處於重設狀態，手勢會執行原生頁面捲動。 </p> <p> 當影像放大時，影像會垂直移動。 如果影像移至檢視邊緣，並且在相同方向上執行滑動，手勢會執行原生頁面捲動。 </p> <p> 如果手勢是在色票區域內完成，則會執行原生頁面捲動。 </p> </td> 
  </tr> 
 </tbody> 
</table>

檢視器支援在Windows裝置上使用觸控螢幕和滑鼠的觸控輸入和滑鼠輸入。 不過，這項支援僅限Chrome、Internet Explorer 11和Edge網頁瀏覽器。

此檢視器可完全透過鍵盤存取。

請參閱 [鍵盤協助功能和導覽](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 內嵌縮放檢視器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同的網頁對檢視器行為有不同的需求。 有時網頁會提供連結，當點按時，會在個別的瀏覽器視窗中開啟檢視器。 在其他情況下，必須將檢視器直接內嵌在代管頁面中。 在後一種情況下，網頁可能具有靜態版面，或使用不同裝置或不同瀏覽器視窗大小顯示不同的互動式設計。 為滿足這些需求，檢視器支援三種主要作業模式： 快顯功能、固定大小內嵌和回應式設計內嵌。

**關於彈出式模式**

在快顯模式中，檢視器會在個別的網頁瀏覽器視窗或標籤中開啟。 它會佔用整個瀏覽器視窗區域，並在調整瀏覽器大小或變更裝置方向時進行調整。

此模式是行動裝置最常見的模式。 網頁會使用 `window.open()` JavaScript呼叫、正確設定的 `A` HTML元素或任何其他適當的方法載入檢視器。

建議您使用現成可用的HTML頁面來建立快顯作業模式。 現成的HTML頁面會呼叫， `ZoomViewer.html` 並位於標準IS- `html5/` Viewer部署的子資料夾下方，如下所示：

`<s7viewers_root>/html5/ZoomViewer.html`

套用自訂CSS，以建立自訂的頁面外觀。

以下是在新視窗中開啟檢視器的HTML程式碼範例：

```
 <a 
href="http://s7d1.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample" 
target="_blank">Open popup viewer</a>
```

**關於固定大小嵌入模式和自適應設計嵌入模式**

在內嵌模式下，檢視器會新增至現有的網頁，其中可能已有與檢視器無關的客戶內容。 檢視器通常只佔據網頁的部分空間。

主要使用案例是針對桌上型電腦或平板電腦裝置的網頁，以及可根據裝置類型自動調整版面的自適應設計頁面。

當檢視器在初始載入後未變更其大小時，會使用固定大小內嵌。 此選項是具有靜態版面的網頁的最佳選擇。

回應式設計內嵌模式會假設檢視器在執行時期必須重新調整大小，因為其容器的大小會改變 `DIV`。 最常見的使用案例是將檢視器新增至使用彈性版面的網頁。

在回應式設計內嵌模式中，檢視器的運作方式視網頁大小容器而有所不同 `DIV`。 如果網頁只設定容器的寬度，而不限制其高度 `DIV`，檢視器會根據所使用資產的外觀比例自動選擇其高度。 此邏輯可確保資產完美整合至檢視中，而不會在側邊產生任何填補空間。 此使用案例最常用於使用自適應版面架構（例如引導、基礎等）的網頁。

如果網頁同時設定檢視器容器的寬度和高度 `DIV`，檢視器會填滿該區域，並遵循網頁提供的大小。 例如，將檢視器內嵌至模態覆蓋中，其中覆蓋會根據網頁瀏覽器視窗大小調整大小。

## 固定大小內嵌 {#section-44f365e6c0dd40709467a459afa82a7f}

您可執行下列動作，將檢視器新增至網頁：

1. 將檢視器JavaScript檔案新增至您的網頁。
1. 定義容器DIV。
1. 設定檢視器大小。
1. 建立和初始化檢視器。

1. 將檢視器JavaScript檔案新增至您的網頁。

   建立檢視器時，您必須在HTML標題中新增指令碼標籤。 在您使用檢視器API之前，請確定您已加入 [!DNL ZoomViewer.js]。 此檔 [!DNL ZoomViewer.js] 案位於標準IS- [!DNL html5/js/] Viewer部署的子資料夾下：

[!DNL <s7viewers_root>/html5/js/ZoomViewer.js]

如果檢視器部署在其中一個Adobe Dynamic Media Classic伺服器上，且是從相同網域提供，則可使用相對路徑。 否則，您會指定安裝IS-Viewer之一的Adobe Dynamic Media Classic伺服器的完整路徑。

相對路徑如下所示：

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/ZoomViewer.js"></script>
```

>[!NOTE]
>
>您只應參考頁面上的主要檢視 `include` 器JavaScript檔案。 您不應在網頁程式碼中參考檢視器邏輯在執行時期中可能下載的任何其他JavaScript檔案。 尤其是，請勿直接參考檢視器從內容路 `Utils.js` 徑載入的HTML5 SDK程 `/s7viewers` 式庫(稱為整合SDK `include`)。 原因是檢視器邏輯可完 `Utils.js` 全管理或類似執行時期檢視器程式庫的位置，而檢視器版本之間的位置也會改變。 Adobe不會在伺服器上保留舊版次 `includes` 要檢視器。
>
>
>因此，將檢視器使用的任何次要JavaScript `include` 直接參考放在頁面上，將來部署新產品版本時，檢視器功能會中斷。

1. 定義容器DIV。

   將空的DIV元素新增至您要檢視器顯示的頁面。 DIV元素必須定義其ID，因為此ID稍後會傳遞至檢視器API。

   預留位置DIV是定位的元素，這表示 `position` CSS屬性已設為 `relative` 或 `absolute`。

   以下是已定義預留位置DIV元素的範例：

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. 設定檢視器大小。

   此檢視器在使用多項目集時，會在案頭系統上顯示縮圖，縮圖會放在主檢視的下方。 同時，檢視器允許在執行時期中使用 `setAsset()` API交換主要資產。 身為開發人員，當新資產只有一個項目時，您可以控制檢視器管理底部縮圖區域的方式。 您可以保持外部檢視器大小的完整性，並讓主檢視器增加其高度並佔用縮圖區域。 或者，您可以將主檢視大小保持為靜態，並收合外部檢視器區域，讓網頁內容向上移動，並使用縮圖中剩餘的免費螢幕空間。

   若要保持外部檢視器邊界不變，請以絕 `.s7zoomviewer` 對單位定義頂層CSS類別的大小。 CSS中的大小可直接放在HTML頁面上，或自訂檢視器CSS檔案中，此檔案稍後會指派給Scene7 Publishing System中的檢視器預設記錄，或使用樣式命令明確傳遞。

   如需使 [用CSS設定檢視器樣式的詳細資訊](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-customizingviewer/c-html5-20-zoom-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) ，請參閱自訂縮放檢視器。

   以下是在HTML頁面中定義靜態外部檢視器大小的範例：

   ```
   #s7viewer.s7zoomviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   您可以在下列範例中查看使用固定外部檢視器的行為。 請注意，當您在集合之間切換時，外部檢視器大小不會變更：

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/ZoomViewer-fixed-outer-area.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/ZoomViewer-fixed-outer-area.html)

   若要讓主檢視尺寸保持靜態，請使用 `Container` CSS選取器或使用修飾元，以絕對單位定義內部 `.s7zoomviewer` SDK元件的檢視器 `.s7container``stagesize` 大小。

   以下範例定義內部 `Container` SDK元件的檢視器大小，以便在切換資產時，主檢視區域不會變更其大小：

   ```
   #s7viewer.s7zoomviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   下列示範頁面顯示具有固定主檢視大小的檢視器行為。 請注意，當您在集合之間切換時，主檢視會保持靜態，而網頁內容會垂直移動。

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/ZoomViewer-fixed-main-view.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/ZoomViewer-fixed-main-view.html)

   您可以在Scene7 Publishing System的檢視器預設記錄中設定修飾元，或以檢視器初始化程式碼與系列明確傳遞修飾元，或以 `stagesize``params` API呼叫的形式傳遞，如本說明的「命令參考」區段中所述，如下所示：

   ```
    zoomViewer.setParam("stagesize", 
   "640,480");
   ```

   建議使用以CSS為基礎的方法，並在此範例中使用。

1. 建立和初始化檢視器。

   完成上述步驟後，您將建立類的實例，將所有配置資訊 `s7viewers.ZoomViewer` 傳遞給其建構子，並在查看器實例 `init()` 上調用方法。

   設定資訊會以JSON物件的形式傳遞至建構函式。 至少，此物件應具有欄 `containerId` 位，其中包含檢視器容器ID的名稱，以及檢視器支援的設定參數巢狀 `params` JSON物件。 在此情況下，物 `params` 件必須至少將影像伺服URL傳遞為屬 `serverUrl` 性，並將初始資產傳遞為 `asset` 參數。 以JSON為基礎的初始化API可讓您使用一行程式碼來建立和啟動檢視器。

   請務必將檢視器容器新增至DOM，如此檢視器程式碼就能依其ID找到容器元素。 有些瀏覽器會延遲建立DOM，直到網頁結束為止。 為獲得最大相容性，請 `init()` 在結束標籤之前或在 `BODY` body事件上呼叫方 `onload()` 法。

   同時，容器元素也不一定是網頁版面的一部分。 例如，它可能會使用指派給它 `display:none` 的樣式隱藏。 在此情況下，檢視器會延遲其初始化程式，直到網頁將容器元素帶回版面為止。 發生此情況時，檢視器載入會自動繼續。

   以下是建立檢視器例項、將最小必要的設定選項傳遞至建構函式，以及呼叫方法的范 `init()` 例。 此範例假 `zoomViewer` 設是檢視器例項、 `s7viewer` 預留位置DIV的名稱、 `http://s7d1.scene7.com/is/image/` 影像伺服URL，以及 `Scene7SharedAssets/ImageSet-Views-Sample` 資產。

   ```
   <script type="text/javascript"> 
   var zoomViewer = new s7viewers.ZoomViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   以下程式碼是內嵌固定大小視訊檢視器之平凡網頁的完整範例：

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7zoomviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var zoomViewer = new s7viewers.ZoomViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

## 不受高度限制的自適應設計內嵌 {#section-b9ca11a7e7aa4f74ab43244cbca37ae0}

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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
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
var zoomViewer = new s7viewers.ZoomViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

下列範例頁面說明在實際使用中，不受高度限制的互動式設計內嵌功能：

[即時展示](https://landing.adobe.com/tw/na/dynamic-media/ctir-2755/live-demos.html)

## 定義寬度和高度的彈性大小內嵌 {#section-3674e6c032594441a6576b7fb1de6e64}

若是定義了寬度和高度的彈性大小內嵌，網頁樣式會有所不同。 它為DIV提供兩種大小， `"holder"` 並將其置於瀏覽器視窗中。 此外，網頁會將元素和元素的大 `HTML` 小設 `BODY` 為100%。

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

其餘的嵌入步驟與不受限高度自適應設計嵌入步驟相同。 產生的範例如下：

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
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
var zoomViewer = new s7viewers.ZoomViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

## 使用基於setter的API進行內嵌 {#section-44e014925f24418b900696003855c0a9}

您可以使用setter-based API和no-args建構函式，而不是使用JSON型初始化。 使用此API建構函式時，不會使用任何參數，而設定參數是使用 `setContainerId()`、 `setParam()``setAsset()` API方法以及個別的JavaScript呼叫來指定。

下列範例說明如何使用固定大小內嵌與setter-based API:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7zoomviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var zoomViewer = new s7viewers.ZoomViewer(); 
zoomViewer.setContainerId("s7viewer"); 
zoomViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
zoomViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
zoomViewer.init(); 
</script> 
</body> 
</html> 
```

