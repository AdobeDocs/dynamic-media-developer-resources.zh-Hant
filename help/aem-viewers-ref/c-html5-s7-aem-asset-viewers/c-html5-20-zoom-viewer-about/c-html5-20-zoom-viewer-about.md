---
description: 縮放檢視器是顯示可縮放影像的影像檢視器。 此檢視器可與影像集搭配使用，且導覽是使用色票完成。 它提供縮放工具、全螢幕支援、色票和可選的關閉按鈕。 專為在桌上型電腦和行動裝置上運作而設計。
keywords: 回應式
solution: Experience Manager
title: Zoom
feature: Dynamic Media Classic，檢視器，SDK/API，縮放
role: Developer,Business Practitioner
exl-id: 81a74026-fb15-4f57-a4c7-1ab005950245
source-git-commit: e6ff4ed80b22e10fc2bd3fac0f4e39bbf5148f8e
workflow-type: tm+mt
source-wordcount: '2404'
ht-degree: 0%

---

# 縮放{#zoom}

縮放檢視器是顯示可縮放影像的影像檢視器。 此檢視器可與影像集搭配使用，且導覽是使用色票完成。 它提供縮放工具、全螢幕支援、色票和可選的關閉按鈕。 專為在桌上型電腦和行動裝置上運作而設計。

>[!NOTE]
>
>此檢視器不支援使用IR（影像轉譯）或UGC（使用者產生的內容）的影像。

檢視器類型502。

請參閱[系統要求和必要條件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

## 示範URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## 使用縮放查看器{#section-e6c68406ecdc4de781df182bbd8088b4}

縮放檢視器代表主要JavaScript檔案和一組協助檔案（單一JavaScript包含此特定檢視器、資產、CSS所使用的所有檢視器SDK元件），由檢視器在執行階段下載。

您可以使用隨IS檢視器提供的生產就緒HTML頁面，或在內嵌模式中使用縮放檢視器，透過記錄的API將其整合至目標網頁。

設定和外觀與其他檢視器的設定和外觀類似。 所有外觀設定都是透過自訂CSS來達成。

請參閱所有檢視器通用的[命令參考 — 設定屬性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)和所有檢視器通用的[命令參考 — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 與縮放查看器{#section-642e66ca38cd4032992840ec6c0b0cd2}交互

縮放檢視器支援下列其他行動應用程式中常見的觸控手勢。 當檢視器無法處理使用者的滑動手勢時，會將事件轉送至網頁瀏覽器，以執行原生頁面捲動。 即使檢視器佔據大部分裝置螢幕區域，這類功能仍可讓使用者導覽頁面。

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>手勢 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>單點擊 </p> </td> 
   <td colname="col2"> <p> 在色票中選取新縮圖。 在主檢視中，會隱藏或顯示使用者介面元素。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>按兩下 </p> </td> 
   <td colname="col2"> <p> 放大到達到最大放大率為止。 下一個雙點觸控手勢會將檢視器重設為初始檢視狀態。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>代號 </p> </td> 
   <td colname="col2"> <p>放大或縮小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>水準滑動或輕觸 </p> </td> 
   <td colname="col2"> <p> 在色板條中的色板清單中滾動。 </p> <p> 如果影像處於重置狀態，且<span class="codeph"> frametransition </span>參數設定為滑動，則資產將隨幻燈片動畫而更改。 對於其他<span class="codeph">幀轉換</span>模式，手勢執行本機頁面滾動。 </p> <p> 如果放大影像，則會水準移動影像。 如果影像被移動到視圖邊緣，並且按相同方向執行滑動，則該手勢執行本機頁面滾動。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直滑動 </p> </td> 
   <td colname="col2"> <p> 如果影像處於重置狀態，該手勢會執行原生頁面捲動。 </p> <p> 放大影像時，會垂直移動影像。 如果影像被移至檢視邊緣，並且按相同方向執行滑動，則手勢會執行原生頁面捲動。 </p> <p> 如果手勢是在色票區域內完成，則會執行原生頁面捲動。 </p> </td> 
  </tr> 
 </tbody> 
</table>

檢視器支援Windows裝置上的觸控輸入和滑鼠輸入，且有觸控式螢幕和滑鼠。 不過，此支援僅限Chrome、Internet Explorer 11和Edge網頁瀏覽器。

此查看器可完全通過鍵盤訪問。

請參閱[鍵盤輔助功能和導航](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 嵌入縮放查看器{#section-6bb5d3c502544ad18a58eafe12a13435}

不同的網頁對檢視者行為有不同的需求。 有時，網頁會提供連結，當按一下連結時，就會在個別瀏覽器視窗中開啟檢視器。 在其他情況下，則需直接將檢視器內嵌在托管頁面中。 在後一種情況下，網頁可能具有靜態版面，或使用在不同裝置上或針對不同瀏覽器視窗大小顯示不同的回應式設計。 為了滿足這些需求，檢視器支援三種主要操作模式：快顯視窗、固定大小內嵌和回應式設計內嵌。

**關於快顯模式**

在快顯模式中，檢視器會在個別的網頁瀏覽器視窗或標籤中開啟。 它會取用整個瀏覽器視窗區域，並在瀏覽器調整大小或裝置方向變更時進行調整。

此模式是行動裝置最常見的模式。 網頁會使用`window.open()` JavaScript呼叫、正確設定的`A` HTML元素或任何其他適當的方法載入檢視器。

建議您對快顯作業模式使用現成可用的HTML頁面。 現成可用的HTML頁面稱為`ZoomViewer.html`，它位於標準IS-Viewers部署的`html5/`子資料夾下，如下所示：

`<s7viewers_root>/html5/ZoomViewer.html`

套用自訂CSS以達到頁面的自訂外觀。

以下是在新視窗中開啟檢視器的HTML程式碼範例：

```
 <a 
href="http://s7d1.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample" 
target="_blank">Open popup viewer</a>
```

**關於固定大小嵌入模式和響應式設計嵌入模式**

在內嵌模式中，檢視器會新增至現有網頁，而現有網頁可能已有與檢視器無關的客戶內容。 瀏覽者通常只佔據網頁的一部分房地產。

主要使用案例是以桌上型電腦或平板電腦裝置為導向的網頁，以及可自動根據裝置類型調整版面的回應式設計頁面。

當檢視器在初始載入後未變更大小時，會使用固定大小內嵌。 此選項是靜態版面的網頁最佳選擇。

回應式設計內嵌模式假設檢視器在執行階段中因容器`DIV`的大小變更而需要重新調整大小。 最常見的使用案例是在使用彈性版面的網頁中新增檢視器。

在回應式設計內嵌模式中，檢視器的運作方式會因網頁大小其容器`DIV`而有所不同。 如果網頁僅設定容器的寬度`DIV`，保持高度不受限制，則檢視器會根據所使用資產的外觀比例自動選擇其高度。 此邏輯可確保資產完全符合檢視，而無須在側邊填補。 此使用案例最常用於使用回應式版面架構(例如Bootstrap、Foundation等)的網頁。

如果網頁同時設定了查看器容器`DIV`的寬度和高度，則查看器會填入該區域，並遵循網頁提供的大小。 例如，將檢視器內嵌至強制回應覆蓋中，其中覆蓋會根據網頁瀏覽器視窗大小來調整大小。

## 固定大小嵌入{#section-44f365e6c0dd40709467a459afa82a7f}

您可以執行下列操作，將檢視器新增至網頁：

1. 將檢視器JavaScript檔案新增至您的網頁。
1. 定義容器DIV。
1. 設定檢視器大小。
1. 建立和初始化檢視器。

1. 將檢視器JavaScript檔案新增至您的網頁。

   建立檢視器需要在HTML標題中新增指令碼標籤。 使用檢視器API之前，請務必加入[!DNL ZoomViewer.js]。 [!DNL ZoomViewer.js]檔案位於標準IS-Viewers部署的[!DNL html5/js/]子資料夾下：

[!DNL <s7viewers_root>/html5/js/ZoomViewer.js]

如果檢視器部署在其中一個AdobeDynamic Media Classic伺服器上，且是從相同網域提供，則可使用相對路徑。 否則，您需指定安裝IS-Viewers之其中一個AdobeDynamic Media Classic伺服器的完整路徑。

相對路徑如下所示：

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/ZoomViewer.js"></script>
```

>[!NOTE]
>
>您只應在頁面上參考主要檢視器JavaScript `include`檔案。 您不應在網頁程式碼中參考任何其他JavaScript檔案，而檢視器邏輯可能會在執行階段下載這些檔案。 尤其是，請勿直接參考檢視器從`/s7viewers`內容路徑（稱為統一SDK `include`）載入的HTML5 SDK `Utils.js`程式庫。 原因在於，`Utils.js`或類似的執行階段檢視器程式庫的位置，是由檢視器的邏輯完全管理，且檢視器版本之間的位置變更。 Adobe不會在伺服器上保留舊版次要檢視器`includes`。
>
>
>因此，將檢視器使用的任何次要JavaScript `include`的直接參考放在頁面上，會在未來部署新產品版本時中斷檢視器的功能。

1. 定義容器DIV。

   將空白的DIV元素新增至您希望檢視器顯示的頁面。 DIV元素必須定義其ID，因為此ID稍後會傳遞至檢視器API。

   預留位置DIV是已定位的元素，這表示`position` CSS屬性已設為`relative`或`absolute`。

   以下是定義預留位置DIV元素的範例：

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. 設定檢視器大小。

   使用多項目集時，此查看器將顯示縮略圖，在案頭系統上，縮略圖將放在主視圖下。 同時，檢視器允許使用`setAsset()` API在執行階段中交換主要資產。 身為開發人員，當新資產只有一個項目時，您可以控制檢視器如何管理底部的縮圖區域。 可以保持外部查看器大小不變，並允許主視圖增加其高度並佔用縮圖區域。 或者，您可以將主檢視大小保持為靜態，並折疊外部檢視器區域，讓網頁內容向上移動，並使用縮圖中剩餘的免費螢幕房產。

   要保持外部查看器界限不變，請以絕對單位定義`.s7zoomviewer`頂級CSS類的大小。 CSS中的大小可以直接放在HTML頁面上，或放在自訂檢視器CSS檔案中，該檔案稍後會指派給Dynamic Media Classic中的檢視器預設集記錄，或使用style命令明確傳遞。

   如需使用CSS來設定檢視器樣式的詳細資訊，請參閱[自訂縮放檢視器](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-customizingviewer/c-html5-20-zoom-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0)。

   以下是在HTML頁面中定義靜態外部檢視器大小的範例：

   ```
   #s7viewer.s7zoomviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   在以下範例中，您可以看到具有固定外部檢視器的行為。 請注意，當您在集之間切換時，外部檢視器大小不會變更：

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-outer-area.html)

   若要將主檢視維度設為靜態，請使用`.s7zoomviewer` `.s7container` CSS選取器，或使用`stagesize`修飾元，以絕對單位定義內部`Container` SDK元件的檢視器大小。

   以下是定義內部`Container` SDK元件的檢視器大小的範例，以便在切換資產時，主檢視區域不會變更其大小：

   ```
   #s7viewer.s7zoomviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   下列示範頁面顯示具有固定主檢視大小的檢視器行為。 請注意，當您在集之間切換時，主檢視會維持靜態，而網頁內容會垂直移動。

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-main-view.html)

   您可以在Dynamic Media Classic的檢視器預設集記錄中設定`stagesize`修飾元，或透過`params`集合以檢視器初始化程式碼明確傳遞，或以API呼叫的形式傳遞，如本說明的「命令參考」區段所述，如下所示：

   ```
    zoomViewer.setParam("stagesize", 
   "640,480");
   ```

   建議使用CSS型方法，此範例中會使用。

1. 建立和初始化檢視器。

   完成上述步驟後，可以建立`s7viewers.ZoomViewer`類的實例，將所有配置資訊傳遞到其建構子，並在查看器實例上調用`init()`方法。

   設定資訊會以JSON物件的形式傳遞至建構函式。 此物件至少應有`containerId`欄位，該欄位包含檢視器容器ID的名稱，並巢狀`params` JSON物件，以及檢視器支援的設定參數。 在此情況下，`params`物件至少必須以`serverUrl`屬性傳遞影像伺服URL，並以`asset`參數傳遞初始資產。 JSON型初始化API可讓您使用一行程式碼來建立和啟動檢視器。

   請務必將檢視器容器新增至DOM，讓檢視器程式碼可以透過其ID來尋找容器元素。 有些瀏覽器會延遲建立DOM，直到網頁結尾為止。 如需最大相容性，請在結尾的`BODY`標籤前，或在內文`onload()`事件上呼叫`init()`方法。

   同時，容器元素還不一定是網頁版面的一部分。 例如，可使用指派給它的`display:none`樣式來隱藏它。 在此情況下，檢視器會延遲其初始化程式，直到網頁將容器元素帶回版面的那一刻為止。 發生此情況時，檢視器載入會自動恢復。

   以下是建立查看器實例、將最小必要配置選項傳遞給建構子並調用`init()`方法的示例。 此範例假設`zoomViewer`是檢視器例項，`s7viewer`是預留位置DIV的名稱，`http://s7d1.scene7.com/is/image/`是影像伺服URL，而`Scene7SharedAssets/ImageSet-Views-Sample`是資產。

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

   以下程式碼是內嵌固定大小視訊檢視器的簡單網頁的完整範例：

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

## 無限制高度{#section-b9ca11a7e7aa4f74ab43244cbca37ae0}的回應式設計內嵌

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

下列範例頁面說明在實際使用中，不受限制高度的回應式設計內嵌：

[即時演示](https://landing.adobe.com/tw/na/dynamic-media/ctir-2755/live-demos.html)

## 具有定義{#section-3674e6c032594441a6576b7fb1de6e64}寬度和高度的靈活大小嵌入

若是定義寬度和高度的彈性內嵌，網頁樣式會有所不同。 它會為`"holder"` DIV提供兩種大小，並在瀏覽器視窗中將其置中。 此外，網頁還將`HTML`和`BODY`元素的大小設定為100%。

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

其餘嵌入步驟與用於具有不受限制高度的響應式設計嵌入的步驟相同。 產生的範例如下：

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

## 使用基於setter的API {#section-44e014925f24418b900696003855c0a9}嵌入

您可以使用setter型API和無目標建構函式，而不使用JSON型初始化。 使用此API建構函式時不會採用任何參數，且會使用具有個別JavaScript呼叫的`setContainerId()`、`setParam()`及`setAsset()` API方法指定設定參數。

以下範例說明如何使用固定大小內嵌搭配setter型API:

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
