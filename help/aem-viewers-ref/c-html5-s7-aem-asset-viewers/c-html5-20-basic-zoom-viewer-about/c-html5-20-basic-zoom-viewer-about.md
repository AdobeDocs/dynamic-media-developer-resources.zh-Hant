---
title: 基本縮放
description: 基本縮放檢視器是顯示單一可縮放影像的影像檢視器。 它提供縮放工具、全螢幕支援和可選的關閉按鈕。 此檢視器是最輕量的。 專為在桌上型電腦和行動裝置上運作而設計。
keywords: 回應式
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: ee15ce21-20c4-428b-9512-050115e4c322
source-git-commit: d5f1f05c36c1cb8a57b5a4bb8a9d066c20e32e75
workflow-type: tm+mt
source-wordcount: '2028'
ht-degree: 0%

---

# 基本縮放{#basic-zoom}

基本縮放檢視器是顯示單一可縮放影像的影像檢視器。 它提供縮放工具、全螢幕支援和可選的關閉按鈕。 此檢視器是最輕量的。 專為在桌上型電腦和行動裝置上運作而設計。

>[!NOTE]
>
>此檢視器不支援使用IR（影像呈現）或UGC（使用者產生的內容）的影像。

檢視器類型501。

請參閱 [系統需求和先決條件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## 示範URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset=Scene7SharedAssets/Backpack_B](https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset=Scene7SharedAssets/Backpack_B)

## 使用基本縮放檢視器 {#section-e6c68406ecdc4de781df182bbd8088b4}

基本縮放檢視器代表一個JavaScript檔案和一組協助檔案，檢視器會在執行階段下載這些檔案。 基本上，它是單一JavaScript包含，搭配此特定檢視器、資產和CSS使用的所有檢視器SDK元件。

您可以使用隨IS檢視器提供的生產就緒HTML頁面，或在內嵌模式中使用基本縮放檢視器，透過記錄的API將其整合至目標網頁。

設定和外觀與其他檢視器的設定和外觀類似。 所有外觀設定都是透過自訂CSS來達成。

請參閱 [所有檢視器通用的命令參考 — 設定屬性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 和 [所有檢視器 — URL通用的命令參考](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 與基本縮放檢視器互動 {#section-642e66ca38cd4032992840ec6c0b0cd2}

基本縮放檢視器支援下列其他行動應用程式中常見的觸控手勢。

當檢視器無法處理使用者的滑動手勢時，會將事件轉送至網頁瀏覽器，以執行原生頁面捲動。 即使檢視器佔據裝置的大部分螢幕區域，這類功能仍可讓使用者導覽頁面。

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
   <td colname="col2"> <p>隱藏或顯示使用者介面元素。 </p> </td> 
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
   <td colname="col1"> <p>揮動 </p> </td> 
   <td colname="col2"> <p> 如果影像處於重設狀態，該手勢會執行原生頁面捲動。 </p> <p> 放大影像時，會移動影像。 如果影像被移動到視圖邊緣，並且沿該方向執行滑動，則該手勢執行本機頁面捲動。 </p> </td> 
  </tr> 
 </tbody> 
</table>

檢視器也支援Windows裝置上的觸控輸入和滑鼠輸入，且具有觸控式螢幕和滑鼠。 不過，此支援僅限Chrome、Internet Explorer 11和Edge網頁瀏覽器。

此查看器可完全通過鍵盤訪問。

請參閱 [鍵盤協助工具和導覽](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## 嵌入基本縮放查看器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同的網頁對檢視者行為有不同的需求。 有時，網頁會提供連結，當選取此連結時，即會在個別瀏覽器視窗中開啟檢視器。 在其他情況下，必須將檢視器直接內嵌在托管頁面中。 在後一種情況下，網頁可能具有靜態頁面版面，或使用在不同裝置上或針對不同瀏覽器視窗大小顯示不同的回應式設計。 為了滿足這些需求，檢視器支援三種主要操作模式：快顯視窗、固定大小內嵌和回應式設計內嵌。

**關於快顯模式**

在快顯模式中，檢視器會在個別的網頁瀏覽器視窗或標籤中開啟。 它會取用整個瀏覽器視窗區域，並在瀏覽器調整大小或裝置方向變更時進行調整。

快顯模式是行動裝置最常見的模式。 網頁會使用 `window.open()` JavaScript呼叫，已正確設定 `A` HTML元素，或任何其他合適的方法。

建議您對快顯操作模式使用現成可用的HTML頁面。 在這種情況下，它稱為 [!DNL BasicZoomViewer.html] 和位於 [!DNL html5/] 標準IS — 檢視器部署的子資料夾：

[!DNL <s7viewers_root>/html5/BasicZoomViewer.html]

您可以套用自訂CSS來達到視覺化自訂。

以下是在新視窗中開啟檢視器的HTML程式碼範例：

```
<a href="http://s7d1.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset=Scene7SharedAssets/Backpack_B" target="_blank">Open popup viewer</a>
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
1. 定義容器DIV。
1. 設定檢視器大小。
1. 建立和初始化檢視器。

1. 將檢視器JavaScript檔案新增至您的網頁。

   建立檢視器需要在HTML標題中新增指令碼標籤。 使用檢視器API之前，請務必加入 [!DNL BasicZoomViewer.js]. 此 [!DNL BasicZoomViewer.js] 檔案位於 [!DNL html5/js/] 標準IS — 檢視器部署的子資料夾：

[!DNL <s7viewers_root>/html5/js/BasicZoomViewer.js]

如果檢視器部署在其中一個Adobe Dynamic Media Classic伺服器上，且是從相同網域提供，則可使用相對路徑。 否則，您會指定安裝IS-Viewers之一Adobe Dynamic Media Classic伺服器的完整路徑。

相對路徑如下所示：

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/BasicZoomViewer.js"></script>
```

>[!NOTE]
>
>僅參考主要檢視器JavaScript `include` 檔案。 請勿在網頁程式碼中參考任何其他JavaScript檔案，這些檔案可能會由檢視器的邏輯在執行階段下載。 尤其是，請勿直接參考HTML5 SDK `Utils.js` 檢視器從 `/s7viewers` 內容路徑（所謂的整合SDK） `include`)。 原因是 `Utils.js` 或者，檢視器的邏輯和檢視器版本之間的位置變更，可完全管理類似的執行階段檢視器程式庫。 Adobe不會保留舊版次要檢視器 `includes` 在伺服器上。
>
>
>因此，請直接參考任何次要JavaScript `include` 若將來部署新產品版本，則檢視器在頁面上使用時會中斷檢視器功能。

1. 定義容器DIV。

   將空白的DIV元素新增至您希望檢視器顯示的頁面。 DIV元素必須定義其ID，因為此ID稍後會傳遞至檢視器API。 DIV的大小是透過CSS指定。

   預留位置DIV是定位的元素，這表示 `position` CSS屬性設為 `relative` 或 `absolute`.

   以下是定義預留位置DIV元素的範例：

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. 設定檢視器大小

   您可以為聲明來設定檢視器的靜態大小 `.s7basiczoomviewer` 頂層CSS類（以絕對單位表示），或使用 `stagesize` 修飾詞。

   將CSS中的大小調整直接放在HTML頁面或自訂檢視器CSS檔案中。 之後，系統會將它指派給Dynamic Media Classic中的檢視器預設集記錄，或使用style命令明確傳遞。

   請參閱 [自訂基本縮放檢視器](../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-customizingviewer/c-html5-20-basic-zoom-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) 以取得有關使用CSS來設定檢視器樣式的詳細資訊。

   以下是在「HTML」頁面中定義靜態檢視器大小的範例：

   ```
   #s7viewer.s7basiczoomviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   您可以設定 `stagesize` 修飾元(在Dynamic Media Classic中的檢視器預設集記錄中)。 或者，您也可以使用檢視器初始化程式碼，以明確的方式傳遞 `params` 集合，或以API呼叫的形式（如命令參考區段所述），如下所示：

   ```
   basicZoomViewer.setParam("stagesize", "640,480");
   ```

   建議使用CSS型方法，此範例中會使用。

1. 建立和初始化檢視器。

   完成上述步驟後，請建立例項 `s7viewers.BasicZoomViewer` 類，將所有配置資訊傳遞到其建構子，並調用 `init()` 方法。 設定資訊會以JSON物件的形式傳遞至建構函式。 此物件至少應具有containerId欄位，該欄位包含檢視器的名稱 `container ID` 和巢狀 `params` 檢視器支援之設定參數的JSON物件。 在此情況下， `params` 物件至少必須以 `serverUrl` 屬性，而初始資產為 `asset` 參數。 JSON型初始化API可讓您使用一行程式碼來建立和啟動檢視器。

   請務必將檢視器容器新增至DOM，讓檢視器程式碼可以透過其ID來尋找容器元素。 有些瀏覽器會延遲建立DOM，直到網頁結尾為止。 如需最大相容性，請呼叫 `init()` 方法 `BODY` 標籤，或在內文上 `onload()` 事件。

   同時，容器元素還不一定是網頁版面的一部分。 例如，您可能會使用 `display:none` 樣式。 在此情況下，檢視器會延遲其初始化程式，直到網頁將容器元素帶回版面的那一刻為止。 發生此事件時，檢視器載入會自動恢復。

   以下是建立檢視器例項的範例，將最低必要的設定選項傳遞至建構函式，並呼叫 `init()` 方法。 此範例假設 `basicZoomViewer` 是檢視器例項； `s7viewer` 是佔位符的名稱 `DIV`; `http://s7d1.scene7.com/is/image/` 是影像伺服URL，且 `Scene7SharedAssets/Backpack_B` 是資產：

   ```
   <script type="text/javascript"> 
   var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/Backpack_B", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   以下代碼是嵌入大小固定的基本縮放查看器的簡單網頁的完整示例：

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/BasicZoomViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7basiczoomviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
    "containerId":"s7viewer", 
    "params":{ 
     "asset":"Scene7SharedAssets/Backpack_B", 
     "serverurl":"http://s7d1.scene7.com/is/image/" 
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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/BasicZoomViewer.js"></script> 
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
var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"Scene7SharedAssets/Backpack_B", 
  "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

下列範例頁面說明在實際使用中，不受限制高度的回應式設計內嵌：

[即時演示](https://landing.adobe.com/tw/na/dynamic-media/ctir-2755/live-demos.html)

**定義寬度和高度的靈活大小嵌入**

如果定義了寬度和高度的彈性內嵌大小，則網頁樣式會有所不同。 它為 `"holder"` DIV並在瀏覽器視窗中將其置中。 此外，網頁會設定 `HTML` 和 `BODY` 100%。

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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/BasicZoomViewer.js"></script> 
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
var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"Scene7SharedAssets/Backpack_B", 
  "serverurl":"http://s7d1.scene7.com/is/image/" 
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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/BasicZoomViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7basiczoomviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var basicZoomViewer = new s7viewers.BasicZoomViewer(); 
basicZoomViewer.setContainerId("s7viewer"); 
basicZoomViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
basicZoomViewer.setAsset("Scene7SharedAssets/Backpack_B"); 
basicZoomViewer.init(); 
</script> 
</body> 
</html>
```
