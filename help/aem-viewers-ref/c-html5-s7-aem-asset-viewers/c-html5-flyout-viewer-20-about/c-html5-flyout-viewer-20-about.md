---
description: 彈出檢視器是影像檢視器。 它會顯示靜態影像，而縮放版本會顯示在使用者啟動的彈出檢視中。 此檢視器可處理影像集，並使用色票進行導覽。 它可在桌上型電腦和行動裝置上運作。
keywords: 回應
solution: Experience Manager
title: 彈出
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '2095'
ht-degree: 0%

---


# 彈出{#flyout}

彈出檢視器是影像檢視器。 它會顯示靜態影像，而縮放版本會顯示在使用者啟動的彈出檢視中。 此檢視器可處理影像集，並使用色票進行導覽。 它可在桌上型電腦和行動裝置上運作。

>[!NOTE]
>
>此檢視器不支援使用IR（影像演算）或UGC（使用者產生的內容）的影像。

檢視器類型為504。

請參閱[系統需求和先決條件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

## 示範URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## 使用彈出檢視器{#section-f21ac23d3f6449ad9765588d69584772}

彈出檢視器代表主要JavaScript檔案和一組輔助檔案（單一JavaScript包含此特定檢視器使用的所有檢視器SDK元件、資產、CSS），由檢視器在執行時期下載

彈出檢視器僅供內嵌使用，這表示它已使用檔案化的API整合在網頁中。 飛出檢視器沒有可立即生產使用的網頁。

設定和外觀設定與其他檢視器類似。 您可以使用自訂CSS來套用外觀設定。

請參閱所有檢視器通用的[命令參考——設定屬性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)和[所有檢視器通用的命令參考- URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 與彈出檢視器互動{#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

彈出檢視器支援其他行動應用程式中常見的單點觸控和多點觸控手勢。

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
   <td colname="col2"> <p> 啟動彈出視圖或主縮放級別和輔助縮放級別之間的更改。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>水準滑動或輕拂 </p> </td> 
   <td colname="col2"> <p> 在色票列中的色票清單中捲動。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直滑動 </p> </td> 
   <td colname="col2"> <p>如果手勢是在色票區域內完成，則會執行原生頁面捲動。 </p> </td> 
  </tr> 
 </tbody> 
</table>

檢視器也支援在Windows裝置上使用觸控螢幕和滑鼠的觸控輸入和滑鼠輸入。 不過，這項支援僅限Chrome、Internet Explorer 11和Edge網頁瀏覽器。

此檢視器可完全透過鍵盤存取。

請參閱[鍵盤協助功能和導覽](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 內嵌彈出檢視器{#section-6bb5d3c502544ad18a58eafe12a13435}

不同的網頁對檢視器行為有不同的需求。 網頁可能具有靜態頁面版面，或使用不同裝置上顯示不同的回應式設計，或針對不同的瀏覽器視窗大小。 為滿足這些需求，檢視器支援兩種主要作業模式：固定大小內嵌和回應式設計內嵌。

當檢視器在初始載入後未變更其大小時，會使用固定大小內嵌模式。 此選項最適合具有靜態頁面版面的網頁。

回應式設計內嵌模式會假設檢視器在執行時期可能需要調整大小，以回應其容器`DIV`的大小變更。 最常見的使用案例是將檢視器新增至使用彈性頁面版面的網頁。

在彈出檢視器中使用回應式設計內嵌模式時，請務必使用`imagereload`參數為主檢視影像指定明確的中斷點。 最理想的情況是，將中斷點與檢視器寬度的中斷點比對，如網頁CSS所指定。

在回應式設計內嵌模式中，檢視器的運作方式會因網頁大小容器`DIV`而異。 如果網頁僅設定容器的寬度`DIV`，而不限制其高度，則檢視器會根據所使用資產的外觀比例自動選擇其高度。 這表示資產完全符合檢視，不會在側邊填入任何間距。 此特殊使用案例最常用於使用互動式設計版面架構(例如Bootstrap、基礎等)的網頁。

否則，如果網頁同時設定檢視器容器`DIV`的寬度和高度，檢視器只會填滿該區域，並遵循網頁版面所提供的大小。 一個好的使用案例範例是將檢視器內嵌至模型覆蓋，其中覆蓋會根據網頁瀏覽器視窗大小而調整大小。

**固定大小內嵌**

您可執行下列動作，將檢視器新增至網頁：

1. 將檢視器JavaScript檔案新增至您的網頁。
1. 定義容器`DIV`。
1. 設定檢視器大小。
1. 建立和初始化檢視器。

1. 將檢視器JavaScript檔案新增至您的網頁。

   建立檢視器時，您必須在HTML標題中新增指令碼標籤。 請務必加入`FlyoutViewer.js`，才能使用檢視器API。 `FlyoutViewer.js` 位於標準IS- [!DNL html5/js/] Viewer部署的下列子資料夾中：

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

如果檢視器部署在其中一個Adobe的Dynamic Media伺服器上，且是從相同網域提供，則可使用相對路徑。 否則，您將指定到安裝IS-Viewer的AdobeDynamic Media伺服器之一的完整路徑。

相對路徑如下所示：

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>您只應在頁面上參考主要檢視器JavaScript `include`檔案。 您不應在網頁程式碼中參考檢視器邏輯在執行時期中可能下載的任何其他JavaScript檔案。 尤其是，請勿直接參考檢視器從`/s7viewers`內容路徑載入的HTML5 SDK `Utils.js`程式庫（稱為統一SDK `include`）。 原因是`Utils.js`或類似的執行時期檢視器程式庫的位置完全由檢視器的邏輯管理，而檢視器版本間的位置也會變更。 Adobe不會在伺服器上保留舊版次要檢視器`includes`。
>
>
>因此，將檢視器使用的任何次要JavaScript `include`直接參考放在頁面上，將來部署新產品版本時，檢視器功能會中斷。

1. 定義容器DIV。

   將空的DIV元素新增至您要檢視器顯示的頁面。 DIV元素必須定義其ID，因為此ID稍後會傳遞至檢視器API。

   預留位置DIV是定位的元素，這表示`position` CSS屬性設為`relative`或`absolute`。

   網頁有責任為預留位置DIV元素指定適當的`z-index`。 如此可確保檢視器的彈出部分會顯示在其他網頁元素上。

   以下是已定義預留位置DIV元素的範例：

   ```
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. 設定檢視器大小。

   使用多項目集時，此檢視器會顯示縮圖。 在案頭系統上，縮圖會放在主檢視的下方。 同時，檢視器允許在執行時期期間使用`setAsset()` API交換主要資產。 身為開發人員，當新資產只有一個項目時，您可以控制檢視器管理底部區域縮圖區域的方式。 您可以保持外部檢視器大小不變，讓主檢視器增加其高度並佔用縮圖區域。 或者，您可以將主檢視大小保持為靜態，並收合外部檢視器區域，讓網頁內容向上移動，然後使用縮圖中剩餘的免費頁面空間。

   若要保持外部檢視器邊界不變，請以絕對單位定義`.s7flyoutviewer`頂層CSS類別的大小。 CSS中的大小可直接放在HTML頁面上，或自訂檢視器CSS檔案中，此檔案稍後會指派給Dynamic Media·Classic中的檢視器預設記錄，或使用樣式命令明確傳遞。

   如需使用CSS設定檢視器樣式的詳細資訊，請參閱[自訂彈出檢視器](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451)。

   以下是在HTML頁面中定義靜態外部檢視器大小的範例：

   ```
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   您可以在下列範例頁面上看到具有固定外部檢視器區域的行為。 請注意，當您在集合之間切換時，外部檢視器大小不會變更：

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-outer-area.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-outer-area.html)

   若要讓主檢視尺寸保持靜態，請使用`.s7flyoutviewer .s7container` CSS選擇器，以絕對單位定義內部`Container` SDK元件的檢視器大小。 此外，您應將預設檢視器CSS中的`.s7flyoutviewer`頂層CSS類別設定為`auto`，以覆寫其定義的固定大小。

   以下範例定義內部`Container` SDK元件的檢視器大小，以便在切換資產時，主檢視區域不會變更其大小：

   ```
   #s7viewer.s7flyoutviewer { 
    width: auto; 
    height: auto; 
   }  
   #s7viewer.s7flyoutviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   下列範例頁面顯示具有固定主檢視大小的檢視器行為。 請注意，當您在集合之間切換時，主檢視會保持靜態，而網頁內容會垂直移動：

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-main-view.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-main-view.html)

   此外，請注意，預設檢視器CSS會為其外部區域提供固定大小。

1. 建立和初始化檢視器。

   完成上述步驟後，您將建立一個`s7viewers.FlyoutViewer`類的實例，將所有配置資訊傳遞給其建構子，並在查看器實例上調用`init()`方法。 設定資訊會以JSON物件的形式傳遞至建構函式。 至少，此物件應具有`containerId`欄位，此欄位包含檢視器容器ID的名稱，並以檢視器支援的組態參數巢狀內嵌`params` JSON物件。 在這種情況下，`params`物件至少必須將「影像伺服URL」傳遞為`serverUrl`屬性，並將初始資產傳遞為`asset`參數。 以JSON為基礎的初始化API可讓您使用單行程式碼來建立和啟動檢視器。

   請務必將檢視器容器新增至DOM，如此檢視器程式碼就能依其ID找到容器元素。 有些瀏覽器會延遲建立DOM，直到網頁結束為止。 為獲得最大相容性，請在`BODY`結束標籤之前或在主體`onload()`事件上調用`init()`方法。

   同時，容器元素也不一定是網頁版面的一部分。 例如，它可能會使用指派給它的`display:none`樣式進行隱藏。 在此情況下，檢視器會延遲其初始化程式，直到網頁將容器元素帶回版面為止。 發生此情況時，檢視器載入會自動繼續。

   以下是建立檢視器例項的範例，將最小必要的設定選項傳遞至建構函式並呼叫`init()`方法。 範例假設`flyoutViewer`為檢視器例項；`s7viewer`是佔位符`DIV`的名稱；`http://s7d1.scene7.com/is/image/`是影像伺服URL;`Scene7SharedAssets/ImageSet-Views-Sample`是資產：

   ```
   <script type="text/javascript"> 
   var flyoutViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   以下程式碼是內嵌固定大小之彈出檢視器之平凡網頁的完整範例：

   ```
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
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;z-index:1;"></div> 
   <script type="text/javascript"> 
   var flyoutViewer = new s7viewers.FlyoutViewer({ 
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

## 不受高度限制的自適應設計內嵌{#section-056cb574713c4d07be6d07cf3c598839}

有了互動式設計內嵌功能，網頁通常就有某種靈活的版面配置，指定檢視器容器`DIV`的執行時期大小。 在下列範例中，假設網頁允許檢視器的容器`DIV`取用40%的網頁瀏覽器視窗大小，而不會限制其高度。 網頁HTML程式碼如下所示：

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

將檢視器新增至此類頁面的步驟類似於固定大小內嵌的步驟。 唯一的區別是，您需要以相對單位設定大小，來覆寫預設檢視器CSS的固定大小。

1. 將檢視器JavaScript檔案新增至您的網頁。
1. 定義容器`DIV`。
1. 設定檢視器大小。
1. 建立和初始化檢視器。

上述所有步驟都與固定大小內嵌相同，但有下列三個例外：

* 將容器`DIV`新增至現有的「holder」 `DIV`;
* 新增具有明確中斷點的`imagereload`參數；
* 而不是使用絕對單位來設定固定檢視器大小，而是使用CSS將檢視器寬度和高度設定為100%，如下所示：

```
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

以下程式碼為完整範例。 請注意，當重新調整瀏覽器大小時，檢視器大小會如何變更，以及檢視器外觀比例如何符合資產。

```
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
var flyoutViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

下列範例頁面說明在實際使用中，不受高度限制的互動式設計內嵌功能：

[即時展示](https://landing.adobe.com/tw/na/dynamic-media/ctir-2755/live-demos.html)

<!-- KEEP (https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html) -->

## 具有定義{#section-0a329016f9414d199039776645c693de}寬度和高度的靈活大小嵌入

若是定義了寬度和高度的彈性大小內嵌，網頁樣式會有所不同。 它為`"holder"` DIV提供兩種大小，並將其置於瀏覽器窗口中。 此外，網頁還將`HTML`和`BODY`元素的大小設為100%。

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
var flyoutViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## 使用基於Setter的API {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}嵌入

您可以使用setter-based API和no-args建構函式，而不是使用JSON型初始化。 使用此API建構函式時，不會使用任何參數，而且設定參數是使用`setContainerId()`、`setParam()`和`setAsset()` API方法，以及個別的JavaScript呼叫來指定。

下列範例說明如何使用固定大小內嵌與setter-based API:

```
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
var flyoutViewer = new s7viewers.FlyoutViewer(); 
flyoutViewer.setContainerId("s7viewer"); 
flyoutViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
flyoutViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
flyoutViewer.init(); 
</script> 
</body> 
</html>
```

