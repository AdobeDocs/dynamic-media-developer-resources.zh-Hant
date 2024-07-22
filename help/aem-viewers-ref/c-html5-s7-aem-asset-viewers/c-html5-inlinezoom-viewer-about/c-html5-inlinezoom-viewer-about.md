---
title: 內嵌縮放
description: 內嵌縮放檢視器是一種影像檢視器。 它會顯示靜態影像，其中當使用者滑過或接觸主檢視時，會顯示該靜態影像上的縮放版本。 此檢視器可搭配影像集使用，並使用色票完成導覽。 專為桌上型電腦和行動裝置所設計。
keywords: 回應式
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 33e661b0-be5e-4d37-af88-47f7bc433c01
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2315'
ht-degree: 0%

---

# 內嵌縮放{#inline-zoom}

內嵌縮放檢視器是一種影像檢視器。 它會顯示靜態影像，其中當使用者滑過或接觸主檢視時，會顯示該靜態影像上的縮放版本。 此檢視器可搭配影像集使用，並使用色票完成導覽。 專為桌上型電腦和行動裝置所設計。

>[!NOTE]
>
>此檢視器不支援使用IR （影像演算）或UGC （使用者產生的內容）的影像。

檢視器型別為504。

請參閱[系統需求和先決條件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

## 示範URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&amp;config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline&amp;stagesize=500,400](https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&amp;config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline&amp;stagesize=500,400)

## 使用內嵌縮放檢視器 {#section-f21ac23d3f6449ad9765588d69584772}

內嵌縮放檢視器代表主要JavaScript檔案和一組協助程式檔案(單一JavaScript包含此特定檢視器使用的所有Viewer SDK元件、資產、CSS)，由檢視器在執行階段下載。

內嵌縮放檢視器可用於快顯視窗模式(使用影像伺服檢視器隨附的生產就緒HTML頁面)或內嵌模式（使用檔案化API整合至目標網頁）。

組態和外觀設定與其他檢視器的組態和外觀設定類似。 您可以使用自訂CSS來套用外觀設計。

檢視所有檢視器通用的[命令參考 — 組態屬性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)和所有檢視器通用的[命令參考 — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 與內嵌縮放檢視器互動 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Inline Zoom Viewer支援其他行動應用程式中常見的單一觸控和多重觸控手勢。

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>手勢 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>點一下滑鼠 </p> </td> 
   <td colname="col2"> <p> 啟動彈出式檢視或在色票中主要和次要縮放等級之間變更，選取新的縮圖。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>水準撥動或輕觸 </p> </td> 
   <td colname="col2"> <p> 在色票列中捲動色票清單。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直撥動 </p> </td> 
   <td colname="col2"> <p>如果該手勢是在色票區域內完成，則會執行原生頁面捲動。 </p> </td> 
  </tr> 
 </tbody> 
</table>

該檢視器也支援在具備觸控熒幕和滑鼠的Windows裝置上進行觸控輸入和滑鼠輸入。 不過，這項支援僅限Chrome、Internet Explorer 11和Edge網頁瀏覽器。

此檢視器可使用完整的鍵盤。

請參閱[鍵盤協助工具與導覽](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 內嵌內嵌縮放檢視器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同的網頁對檢視者的行為有不同的需求。 有時，網頁會提供可點按的連結，在個別瀏覽器視窗中開啟檢視器。 在其他情況下，可能需要直接將檢視器內嵌在託管頁面中。 在後一種情況下，網頁可能會有靜態頁面佈局，或使用在不同裝置上或不同瀏覽器視窗大小上顯示不同的回應式設計。 為因應這些需求，檢視器支援三種主要操作模式：快顯視窗、固定大小內嵌和回應式內嵌。

**快顯視窗**

在快顯視窗模式中，檢視器會在個別的網頁瀏覽器視窗或標籤中開啟。 它會取用整個瀏覽器視窗區域，並在瀏覽器視窗調整大小或裝置方向變更時進行調整。

此模式在行動裝置中最常見。 網頁會使用`window.open()` JavaScript呼叫、正確設定的`A`HTML元素或任何其他適當的方式載入檢視器。

建議您將現成的HTML頁面用於名為`FlyoutViewer.html`的快顯視窗模式。 它位於標準Image Serving-Viewers部署的[!DNL html5/]子資料夾下：

`<s7viewers_root>/html5/FlyoutViewer.html`

也必須將FlyoutZoomView元件設定為可在內嵌縮放模式中運作。 建議您使用內嵌縮放檢視器的現成可用`Scene7SharedAssets/Universal_HTML5_Zoom_Inline`預設集，或是自訂預設集衍生的預設集。 可套用自訂CSS以達成視覺化自訂。

以下是在新視窗中開啟檢視器的HTML程式碼範例：

```html {.line-numbers}
 <a href="http://s7d1.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline"target="_blank">Open popup viewer</a>
```

**固定大小內嵌與回應式內嵌**

在內嵌模式中，檢視器會新增至現有網頁，其中可能已有某些與檢視器無關的客戶內容。 檢視器通常只佔用網頁不動產的一部分。

主要使用案例是桌上型電腦或平板電腦裝置導向的網頁，以及可依裝置型別自動調整版面的回應式網頁。

當檢視器在初始載入後未變更其大小時，使用固定大小內嵌模式。 此選項最適合使用具有靜態頁面配置的網頁。

回應式設計內嵌模式假設檢視器必須在執行階段調整大小，以回應其容器`DIV`的大小變更。 最常見的使用案例是將檢視器新增到使用彈性頁面配置的網頁。

搭配內嵌縮放檢視器使用回應式設計內嵌模式時，請務必使用`imagereload`引數為主檢視影像指定明確的中斷點。 理想情況下，請將中斷點與網頁CSS指定的檢視器寬度中斷點比對。

在回應式設計內嵌模式中，檢視器的行為會根據網頁容器`DIV`的大小而有所不同。 如果網頁僅設定容器`DIV`的寬度，而不限制其高度，則檢視器會根據所使用資產的外觀比例，自動選擇其高度。 這項功能表示資產可完美地配合檢視，且兩側沒有任何邊框間距。 此特定使用案例最常用於使用回應式設計配置架構(例如Bootstrap或Foundation)的網頁。

否則，如果網頁同時設定檢視器容器`DIV`的寬度和高度，則檢視器只會填滿該區域，並遵循網頁配置所提供的大小。 好的使用案例範例是將檢視器內嵌到強制回應覆蓋圖中，其中覆蓋圖會根據網頁瀏覽器視窗大小調整大小。

**固定大小內嵌**

您可以執行下列動作，將檢視器新增至網頁：

1. 正在將viewer JavaScript檔案新增至您的網頁。
1. 定義容器`DIV`。
1. 設定檢視器大小。
1. 正在建立和初始化檢視器。

1. 正在將viewer JavaScript檔案新增至您的網頁。

   建立檢視器需要您在HTML標題中新增指令碼標籤。 在可以使用檢視器API之前，請確定您已包含`FlyoutViewer.js`。 `FlyoutViewer.js`位於您標準IS-Viewers部署的以下[!DNL html5/js/]子資料夾中：

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

如果檢視器部署在其中一個部署的Dynamic Media伺服器上，且從相同網域提供，則Adobe可以使用相對路徑。 否則，您可以指定已安裝IS-Viewers的其中一個AdobeDynamic Media伺服器的完整路徑。

相對路徑如下所示：

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>僅參考頁面上的主要檢視器JavaScript `include`檔案。 請勿在網頁程式碼中參考任何其他JavaScript檔案（這些檔案可能由執行階段的檢視器邏輯下載）。 特別是，請勿直接參考檢視器從`/s7viewers`內容路徑（所謂整合SDK `include`）載入的HTML5 SDK `Utils.js`資料庫。 原因在於`Utils.js`或類似的執行階段檢視器程式庫的位置完全由檢視器的邏輯管理，且位置會在檢視器發行版本之間變更。 Adobe不會在伺服器上保留舊版的次要檢視器`includes`。
>
>
>因此，日後部署新產品版本時，將檢視器使用的任何次要JavaScript `include`的直接參照放在頁面上，會中斷檢視器功能。

1. 定義容器DIV。

   新增空的DIV元素至要顯示檢視器的頁面。 DIV元素必須定義其ID，因為此ID稍後會傳遞至檢視器API。

   預留位置DIV是定位元素，表示`position` CSS屬性設定為`relative`或`absolute`。

   網頁有責任為預留位置DIV元素指定適當的`z-index`。 這麼做可確保檢視器的彈出式部分出現在其他網頁元素上方。

   以下為已定義預留位置DIV元素的範例：

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. 設定檢視器大小。

   此檢視器在處理多專案集時會顯示縮圖。 在桌上型電腦系統上，縮圖會放置在主要檢視的下方。 同時，檢視器允許在執行階段使用`setAsset()` API交換主要資產。 若新資產只有一個專案，身為開發人員，您可以控制檢視器管理底部區域縮圖區域的方式。 可以保持外部檢視器大小不變，並讓主檢視增加其高度並佔據縮圖區域。 或者，您可以讓主要檢視大小保持靜態，並摺疊外部檢視器區域，讓網頁內容向上移動，然後使用縮圖剩下的自由頁面空間。

   若要保持外部檢視器界限不變，請以絕對單位定義`.s7flyoutviewer`最上層CSS類別的大小。 CSS的大小調整可直接放在HTML頁面或自訂檢視器CSS檔案中，並於稍後指派給Dynamic Media Classic中的檢視器預設集記錄，或使用style命令明確傳遞。

   請參閱[自訂內嵌縮放檢視器](../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-customizingviewer/c-html5-inlinezoom-viewer-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451)，以取得使用CSS設定檢視器樣式的詳細資訊。

   以下是在HTML頁面中定義靜態外部檢視器大小的範例：

   ```html {.line-numbers}
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   您可以在下列範例頁面上看到具有固定外部檢視器區域的行為。 請注意，當您在組之間切換時，外部檢視器大小不會變更：

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-outer-area.html)

   若要將主要檢視維度設為靜態，請使用`.s7flyoutviewer .s7container` CSS選取器以絕對單位定義內部`Container` SDK元件的檢視器大小。 此外，您應將預設檢視器CSS設定為`auto`，以覆寫為`.s7flyoutviewer`最上層CSS類別定義的固定大小。

   以下範例說明如何為內部`Container` SDK元件定義檢視器大小，以便在切換資產時，主要檢視區域不會變更其大小：

   ```html {.line-numbers}
   #s7viewer.s7flyoutviewer { 
    width: auto; 
    height: auto; 
   }  
   #s7viewer.s7flyoutviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   以下範例頁面顯示具有固定主檢視大小的檢視器行為。 請注意，當您在組之間切換時，主要檢視會維持靜態，而網頁內容會垂直移動：

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-main-view.html)

   此外，預設的檢視器CSS可立即為其外部區域提供固定大小。

1. 正在建立和初始化檢視器。

   完成上述步驟後，您會建立`s7viewers.FlyoutViewer`類別的執行個體、將所有組態資訊傳遞至其建構函式，並在檢視器執行個體上呼叫`init()`方法。 組態資訊會以JSON物件的形式傳遞至建構函式。 此物件至少應有`containerId`欄位，其中儲存檢視器容器ID的名稱，以及巢狀`params` JSON物件，其中包含檢視器支援的設定引數。 在此情況下，`params`物件必須至少將影像伺服URL作為`serverUrl`屬性傳遞；初始資產作為`asset`引數，用於載入CSS作為`contentUrl`引數的基底路徑，以及預設名稱作為`config`引數。 JSON型初始化API可讓您使用一行程式碼來建立和啟動檢視器。

   請務必將檢視器容器新增至DOM，讓檢視器程式碼可依其ID尋找容器元素。 有些瀏覽器會延遲建立DOM，直到網頁結尾為止。 為達到最大相容性，請在結尾的`BODY`標籤前面或內文`onload()`事件上呼叫`init()`方法。

   同時，容器元素也不一定屬於網頁版面配置的一部分。 例如，可以使用指派給它的`display:none`樣式來隱藏它。 在此情況下，檢視器會延遲其初始化程式，直到網頁將容器元素帶回版面配置為止。 當此動作發生時，檢視器載入會自動繼續。

   以下是建立檢視器執行個體、將最低必要組態選項傳遞至建構函式並呼叫`init()`方法的範例。 此範例假設`inlineZoomViewer`為檢視器執行個體；`s7viewer`為預留位置`DIV`的名稱；`http://s7d1.scene7.com/is/image/`為影像伺服URL；`Scene7SharedAssets/ImageSet-Views-Sample`為資產：

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
   "config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
   "contenturl" : "http://s7d1.scene7.com/is/content/", 
   "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   下列程式碼為簡單網頁的完整範例，此網頁以固定大小內嵌內嵌縮放檢視器：

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head><body> 
   <div id="s7viewer" style="position:relative;z-index:1;"></div> 
   <script type="text/javascript"> 
   var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
   "config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
   "contenturl" : "http://s7d1.scene7.com/is/content/", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

## 高度不受限制的回應式設計內嵌 {#section-056cb574713c4d07be6d07cf3c598839}

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

將檢視器新增至這類頁面，類似於固定大小內嵌的步驟。 唯一的差異是，您必須以相對單位設定的大小覆寫預設檢視器CSS的固定大小。

1. 正在將viewer JavaScript檔案新增至您的網頁。
1. 定義容器`DIV`。
1. 設定檢視器大小。
1. 正在建立和初始化檢視器。

上述所有步驟與嵌入固定大小相同，但有以下三個例外：

* 將容器`DIV`新增至現有的「持有者」`DIV`；
* 已新增具有明確中斷點的`imagereload`引數；
* 不是使用絕對單位來設定固定的檢視器大小，而是使用將檢視器`width`和`height`設定為100%的CSS，如下所示：

```html {.line-numbers}
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

下列程式碼為完整的範例。 請注意瀏覽器調整大小時檢視器大小的變化，以及檢視器外觀比例與資產的相符情形。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative;z-index:1"></div> 
</div> 
<script type="text/javascript"> 
var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
"config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
"contenturl" : "http://s7d1.scene7.com/is/content/", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

以下範例頁面說明高度不受限制的回應式設計內嵌在實際應用中的更多情況：

[即時示範](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[備用示範位置](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

## 定義寬度和高度的彈性大小內嵌 {#section-0a329016f9414d199039776645c693de}

如果有已定義寬度和高度的彈性大小內嵌，則網頁樣式會不同。 它同時提供大小給`"holder"` DIV，並將它置中於瀏覽器視窗中。 此外，網頁會將`HTML`和`BODY`專案的大小設定為100%。

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

其餘的嵌入步驟與用於高度不受限制的回應式設計嵌入的步驟相同。 產生的範例如下：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
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
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative;z-index:1"></div> 
</div> 
<script type="text/javascript"> 
var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
"config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
"contenturl" : "http://s7d1.scene7.com/is/content/", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## 使用Setter型API進行內嵌 {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

除了使用JSON型初始化之外，也可以使用setter型API和no-args建構函式。 使用此API建構函式不會接受任何引數，而設定引數是使用`setContainerId()`、`setParam()`和`setAsset()` API方法，以及個別的JavaScript呼叫所指定。

下列範例說明如何將固定大小內嵌與setter型API搭配使用：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7flyoutviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head><body> 
<div id="s7viewer" style="position:relative;z-index:1;"></div> 
<script type="text/javascript"> 
var inlineZoomViewer = new s7viewers.FlyoutViewer(); 
inlineZoomViewer.setContainerId("s7viewer"); 
inlineZoomViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
inlineZoomViewer.setParam("config", "Scene7SharedAssets/Universal_HTML5_Zoom_Inline"); 
inlineZoomViewer.setParam("contenturl", "http://s7d1.scene7.com/is/content/"); 
inlineZoomViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
inlineZoomViewer.init(); 
</script> 
</body> 
</html>
```
