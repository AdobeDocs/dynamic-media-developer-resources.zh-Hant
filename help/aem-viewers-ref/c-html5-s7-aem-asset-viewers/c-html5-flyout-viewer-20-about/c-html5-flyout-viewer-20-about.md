---
description: 彈出查看器是影像查看器。 它會顯示靜態影像，其縮放版本顯示在使用者啟動的彈出檢視中。 此檢視器可與影像集搭配使用，且導覽是使用色票完成。 專為在桌上型電腦和行動裝置上運作而設計。
keywords: 回應式
solution: Experience Manager
title: 彈出
feature: Dynamic Media Classic，檢視器，SDK/API,Flyout
role: Developer,Business Practitioner
exl-id: 9b60330f-5348-431d-9682-cf97aace3679
source-git-commit: e6ff4ed80b22e10fc2bd3fac0f4e39bbf5148f8e
workflow-type: tm+mt
source-wordcount: '2084'
ht-degree: 0%

---

# 彈出{#flyout}

彈出查看器是影像查看器。 它會顯示靜態影像，其縮放版本顯示在使用者啟動的彈出檢視中。 此檢視器可與影像集搭配使用，且導覽是使用色票完成。 專為在桌上型電腦和行動裝置上運作而設計。

>[!NOTE]
>
>此檢視器不支援使用IR（影像轉譯）或UGC（使用者產生的內容）的影像。

檢視器類型為504。

請參閱[系統要求和必要條件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

## 示範URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## 使用彈出查看器{#section-f21ac23d3f6449ad9765588d69584772}

彈出檢視器代表主要JavaScript檔案和一組協助檔案（單一JavaScript包含此特定檢視器、資產、CSS所使用的所有檢視器SDK元件），由檢視器在執行階段下載

彈出檢視器僅用於內嵌用途，這表示它已使用記錄的API整合至網頁中。 飛出檢視器沒有生產就緒網頁可用。

設定和外觀與其他檢視器的設定和外觀類似。 您可以使用自訂CSS來套用外觀。

請參閱所有檢視器通用的[命令參考 — 設定屬性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)和所有檢視器通用的[命令參考 — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 與彈出查看器{#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}交互

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
   <td colname="col1"> <p>單點擊 </p> </td> 
   <td colname="col2"> <p> 激活彈出視圖或主縮放級別和次縮放級別之間的更改。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>水準滑動或輕觸 </p> </td> 
   <td colname="col2"> <p> 在色板條中的色板清單中滾動。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直滑動 </p> </td> 
   <td colname="col2"> <p>如果手勢是在色票區域內完成，則會執行原生頁面捲動。 </p> </td> 
  </tr> 
 </tbody> 
</table>

檢視器也支援Windows裝置上的觸控式輸入和滑鼠輸入，且具有觸控式螢幕和滑鼠。 不過，此支援僅限Chrome、Internet Explorer 11和Edge網頁瀏覽器。

此查看器可完全通過鍵盤訪問。

請參閱[鍵盤輔助功能和導航](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 嵌入彈出查看器{#section-6bb5d3c502544ad18a58eafe12a13435}

不同的網頁對檢視者行為有不同的需求。 網頁可能具有靜態頁面版面，或使用在不同裝置上以不同方式顯示的回應式設計，或針對不同瀏覽器視窗大小。 為了滿足這些需求，檢視器支援兩種主要操作模式：固定大小內嵌和回應式設計內嵌。

當檢視器在初始載入後未變更其大小時，會使用固定大小內嵌模式。 此選項最適用於具有靜態頁面配置的網頁。

回應式設計內嵌模式假設檢視器在執行階段可能需要調整大小，以回應其容器`DIV`的大小變更。 最常見的使用案例是在使用彈性頁面版面的網頁中新增檢視器。

搭配彈出檢視器使用回應式設計內嵌模式時，請務必使用`imagereload`參數為主檢視影像指定明確的中斷點。 理想情況下，請將斷點與網頁CSS指定的查看器寬度斷點相匹配。

在回應式設計內嵌模式中，檢視器的運作方式會因網頁大小其容器`DIV`而有所不同。 如果網頁僅設定容器的寬度`DIV`，保持高度不受限制，則檢視器會根據所使用資產的外觀比例自動選擇其高度。 這表示資產可完美地貼入檢視中，側邊不需任何邊框間距。 此特定使用案例最常用於使用回應式設計配置架構(例如Bootstrap、Foundation等)的網頁。

否則，如果網頁同時設定了查看器容器`DIV`的寬度和高度，則查看器只填入該區域，並遵循網頁佈局提供的大小。 一個很好的使用案例範例是將檢視器內嵌至強制回應覆蓋中，其中覆蓋會根據網頁瀏覽器視窗大小來調整大小。

**固定大小嵌入**

您可以執行下列操作，將檢視器新增至網頁：

1. 將檢視器JavaScript檔案新增至您的網頁。
1. 定義容器`DIV`。
1. 設定檢視器大小。
1. 建立和初始化檢視器。

1. 將檢視器JavaScript檔案新增至您的網頁。

   建立檢視器需要在HTML標題中新增指令碼標籤。 使用檢視器API之前，請務必加入`FlyoutViewer.js`。 `FlyoutViewer.js` 位於標準IS- [!DNL html5/js/] 檢視器部署的下列子資料夾中：

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

如果檢視器部署在其中一個AdobeDynamic Media伺服器上，且是從相同網域提供，則可使用相對路徑。 否則，您將指定安裝IS-Viewers之一的AdobeDynamic Media伺服器的完整路徑。

相對路徑如下所示：

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
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

   網頁有責任為預留位置DIV元素指定正確的`z-index`。 這麼做可確保檢視器的彈出部分出現在其他網頁元素的頂端。

   以下是定義預留位置DIV元素的範例：

   ```
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. 設定檢視器大小。

   使用多項目集時，此檢視器會顯示縮圖。 在案頭系統上，縮圖會放在主檢視下方。 同時，檢視器允許使用`setAsset()` API在執行階段交換主要資產。 身為開發人員，當新資產只有一個項目時，您可以控制檢視器如何管理底部區域的縮圖區域。 可以保持外部查看器大小不變，並允許主視圖增加其高度並佔用縮圖區域。 或者，您可以將主檢視大小保持為靜態，並折疊外部檢視器區域，從而讓網頁內容向上移動，然後使用縮圖中剩餘的免費頁面空間。

   要保持外部查看器邊界不變，請以絕對單位定義`.s7flyoutviewer`頂級CSS類的大小。 CSS中的大小可以直接放在HTML頁面上，或放在自訂檢視器CSS檔案中，該檔案稍後會指派給Dynamic Media Classic中的檢視器預設集記錄，或使用style命令明確傳遞。

   如需使用CSS來設定檢視器樣式的詳細資訊，請參閱[自訂彈出檢視器](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451)。

   以下是在HTML頁面中定義靜態外部檢視器大小的範例：

   ```
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   您可以在下列範例頁面上看到具有固定外部檢視器區域的行為。 請注意，當您在集之間切換時，外部檢視器大小不會變更：

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-outer-area.html)

   若要將主檢視維度設為靜態，請使用`.s7flyoutviewer .s7container` CSS選取器，以內部`Container` SDK元件的絕對單位定義檢視器大小。 此外，您應將預設檢視器CSS的`.s7flyoutviewer`頂層CSS類別設定為`auto`，以覆寫該類別所定義的固定大小。

   以下是定義內部`Container` SDK元件的檢視器大小的範例，以便在切換資產時，主檢視區域不會變更其大小：

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

   以下範例頁面顯示具有固定主檢視大小的檢視器行為。 請注意，當您在集之間切換時，主檢視會維持靜態，而網頁內容會垂直移動：

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-main-view.html)

   另請注意，預設檢視器CSS會為其外部區域提供固定大小。

1. 建立和初始化檢視器。

   完成上述步驟後，可以建立`s7viewers.FlyoutViewer`類的實例，將所有配置資訊傳遞到其建構子，並在查看器實例上調用`init()`方法。 設定資訊會以JSON物件的形式傳遞至建構函式。 此物件至少應有`containerId`欄位，該欄位包含檢視器容器ID的名稱，並以檢視器支援的設定參數巢狀`params` JSON物件。 在此情況下，`params`物件至少必須以`serverUrl`屬性傳遞影像伺服URL，並以`asset`參數傳遞初始資產。 JSON型初始化API可讓您使用一行程式碼來建立和啟動檢視器。

   請務必將檢視器容器新增至DOM，讓檢視器程式碼可以透過其ID來尋找容器元素。 有些瀏覽器會延遲建立DOM，直到網頁結尾為止。 如需最大相容性，請在結尾的`BODY`標籤前，或在內文`onload()`事件上呼叫`init()`方法。

   同時，容器元素還不一定是網頁版面的一部分。 例如，可使用指派給它的`display:none`樣式來隱藏它。 在此情況下，檢視器會延遲其初始化程式，直到網頁將容器元素帶回版面的那一刻為止。 發生此情況時，檢視器載入會自動繼續。

   以下是建立查看器實例的示例，將最小必要配置選項傳遞給建構子並調用`init()`方法。 此範例假設`flyoutViewer`為檢視器例項；`s7viewer`是佔位符`DIV`的名稱；`http://s7d1.scene7.com/is/image/`是影像伺服URL;且`Scene7SharedAssets/ImageSet-Views-Sample`為資產：

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

   以下程式碼是內嵌具有固定大小的彈出檢視器的簡單網頁的完整範例：

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

## 無限制高度{#section-056cb574713c4d07be6d07cf3c598839}的回應式設計內嵌

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

將檢視器新增至此類頁麵類似於固定大小內嵌的步驟。 唯一的差異是，您需要以相對單位設定大小，來覆寫預設檢視器CSS的固定大小。

1. 將檢視器JavaScript檔案新增至您的網頁。
1. 定義容器`DIV`。
1. 設定檢視器大小。
1. 建立和初始化檢視器。

上述所有步驟與固定大小嵌入相同，但有以下三個例外：

* 將容器`DIV`添加到現有的「holder」 `DIV`;
* 新增`imagereload`參數，其中包含明確斷點；
* 不使用絕對單位來設定固定的檢視器大小，而是使用CSS將檢視器寬度和高度設為100%，如下所示：

```
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

下列程式碼為完整的範例。 注意當瀏覽器調整大小時，檢視器大小會如何變更，以及檢視器外觀比例與資產如何相符。

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

下列範例頁面說明在實際使用中，不受限制高度的回應式設計內嵌：

[即時演示](https://landing.adobe.com/tw/na/dynamic-media/ctir-2755/live-demos.html)

[替代演示位置](https://experienceleague.adobe.com/tools/vlist/vlist.html)

## 具有定義{#section-0a329016f9414d199039776645c693de}的寬度和高度的靈活大小嵌入

若是定義寬度和高度的彈性內嵌，網頁樣式會有所不同。 它會為`"holder"` DIV提供兩種大小，並將其置於瀏覽器視窗中。 此外，網頁還將`HTML`和`BODY`元素的大小設定為100%。

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

您可以使用setter型API和無目標建構函式，而不使用JSON型初始化。 使用此API建構函式時不會採用任何參數，且會使用`setContainerId()`、`setParam()`及`setAsset()` API方法（搭配個別的JavaScript呼叫）指定設定參數。

以下範例說明如何使用固定大小內嵌搭配setter型API:

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
