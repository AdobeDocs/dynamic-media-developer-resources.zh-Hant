---
description: eCatalog Search Viewer是一種目錄檢視器，可依跨頁或逐頁顯示電子手冊。eCatalog可讓使用者使用其他使用者介面元素或專用的縮圖模式，來瀏覽目錄。 使用者也可以放大每個頁面，以取得更詳細的資訊。
keywords: responsive
seo-description: eCatalog Search Viewer是一種目錄檢視器，可依跨頁或逐頁顯示電子手冊。eCatalog可讓使用者使用其他使用者介面元素或專用的縮圖模式，來瀏覽目錄。 使用者也可以放大每個頁面，以取得更詳細的資訊。
seo-title: eCatalog搜尋
solution: Experience Manager
title: eCatalog搜尋
topic: Dynamic media
uuid: f5ec33bf-e827-4709-9780-6f17096bf306
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '2228'
ht-degree: 0%

---


# eCatalog搜尋{#ecatalog-search}

eCatalog Search Viewer是一種目錄檢視器，可依跨頁或逐頁顯示電子手冊。eCatalog可讓使用者使用其他使用者介面元素或專用的縮圖模式，來瀏覽目錄。 使用者也可以放大每個頁面，以取得更詳細的資訊。

此檢視器可與Ecatalog搭配使用，並支援選用的影像地圖和社交共用工具。 它提供縮放工具、型錄導覽工具、全螢幕支援、縮圖和選購的關閉按鈕。 檢視器也支援社交分享工具、列印、下載和我的最愛。 它可在桌上型電腦和行動裝置上運作。

用戶還可以對目錄內容執行基於關鍵字或基於短語的搜索。

>[!NOTE]
>
>此檢視器不支援使用IR（影像演算）或UGC（使用者產生的內容）的影像。

檢視器類型513。

請參 [閱系統需求和先決條件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

## 示範URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&amp;serverUrl=https://s7d9.scene7.com/is/image/&amp;config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&amp;contenturl=https://s7d9.scene7.com/skins/&amp;asset=Viewers/Pluralist&amp;searchserverurl=https://s7search1.scene7.com/s7search/](https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&amp;serverUrl=https://s7d9.scene7.com/is/image/&amp;config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&amp;contenturl=https://s7d9.scene7.com/skins/&amp;asset=Viewers/Pluralist&amp;searchserverurl=https://s7search1.scene7.com/s7search/)

## 使用eCatalog檢視器 {#section-e6c68406ecdc4de781df182bbd8088b4}

eCatalog搜尋檢視器代表主要JavaScript檔案和一組輔助檔案（單一JavaScript包含此特定檢視器使用的所有檢視器SDK元件、資產、CSS），由檢視器在執行時期中下載

您可以使用隨IS檢視器提供的可立即生產使用的HTML頁面，或在內嵌模式下，以快顯模式使用eCatalog Search Viewer，在內嵌模式下，使用檔案化的API將其整合至目標網頁。

設定和外觀設定與其他檢視器類似。 所有外觀設定都是透過自訂CSS來完成。

請參 [閱所有檢視器通用的命令參考——所有檢視器通用的組態屬性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)[和命令參考- URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 與eCatalog Search Viewer互動 {#section-642e66ca38cd4032992840ec6c0b0cd2}

eCatalog Search Viewer支援下列觸控手勢，這些手勢在其他行動應用程式中很常見。

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
   <td colname="col2"> <p> 在色票中選取新的縮圖。 </p> </td> 
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
   <td colname="col2"> <p>如果使用投影片影格轉場，請捲動目錄頁面清單。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直滑動或輕拂 </p> </td> 
   <td colname="col2"> <p>當影像處於重設狀態時，會執行原生頁面捲動。 </p> <p>當縮圖處於作用中時，會捲動縮圖清單。 </p> </td> 
  </tr> 
 </tbody> 
</table>

可啟用逼真的頁面翻轉動畫效果，以便在目錄頁面之間導覽。 在這種情況下，使用者可以按住並拖曳頁面角落，並翻轉頁面。

此檢視器也支援在Windows裝置上使用觸控螢幕和滑鼠的觸控輸入和滑鼠輸入。 不過，這項支援僅限Chrome、Internet Explorer 11和Edge網頁瀏覽器。

## 使用eCatalog Search Viewer的社交媒體分享工具 {#section-eb575084a99647c3a9591f439f40b412}

eCatalog Search Viewer支援社交共用工具。這些工具是主控制列中的按鈕，當使用者按一下或點選時，會展開為共用工具列。

共用工具列包含支援之每種共用管道類型的圖示，包括Facebook、Twitter、電子郵件共用、內嵌代碼共用和連結共用。 當啟用電子郵件共用、內嵌共用或連結共用工具時，檢視器會顯示包含對應資料輸入表單的強制對話方塊。 呼叫Facebook或Twitter時，檢視器會從社交服務將使用者重新導向至標準分享對話方塊。 由於網頁瀏覽器的安全性限制，共用工具無法在全螢幕模式下使用。

檢視器的「搜尋」功能在主工具列中提供為外觀玻璃圖示。 按一下或點選圖示會啟動「搜尋」面板並含輸入欄位。 在輸入關鍵字或片語並按Enter後，檢視器會在面板中呈現搜尋結果，並反白顯示主檢視中找到的字詞。

## 內嵌eCatalog Search檢視器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同的網頁對檢視器行為有不同的需求。 有時網頁會提供連結，當點按時，會在個別的瀏覽器視窗中開啟檢視器。 在其他情況下，必須直接將檢視器內嵌在代管頁面中。 在後一種情況下，網頁可能具有靜態頁面版面，或使用不同裝置或不同瀏覽器視窗大小顯示不同的互動式設計。 為滿足這些需求，檢視器支援三種主要作業模式： 快顯功能、固定大小內嵌和回應式設計內嵌。

**關於彈出式模式**

在快顯模式中，檢視器會在個別的網頁瀏覽器視窗或標籤中開啟。 它會佔用整個瀏覽器視窗區域，並在瀏覽器調整大小或行動裝置的方向變更時進行調整。

快顯模式是行動裝置最常見的模式。 網頁會使用 `window.open()` JavaScript呼叫、正確設定的 `A` HTML元素或任何其他適當的方法載入檢視器。

建議您使用現成可用的HTML頁面來進行快顯作業模式。 在這種情況下，它會被呼叫， [!DNL eCatalogSearchViewer.html] 並位於標準IS- [!DNL html5/] Viewer部署的子資料夾中：

[!DNL <s7viewers_root>/html5/eCatalogSearchViewer.html]

您可以套用自訂CSS，以實現視覺化自訂。

以下是在新視窗中開啟檢視器的HTML程式碼範例：

```
<a href="https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&serverUrl=https://s7d9.scene7.com/is/image/&config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&contenturl=https://s7d9.scene7.com/skins/&asset=Viewers/Pluralist&searchserverurl=https://s7search1.scene7.com/s7search/" target="_blank">Open pop-up viewer</a>
```

**關於固定大小嵌入模式和自適應設計嵌入模式**

在內嵌模式中，檢視器會新增至現有的網頁，而現有網頁可能已有與檢視器無關的客戶內容。 檢視器通常只佔用網頁的部分空間。

主要使用案例是針對桌上型電腦或平板電腦裝置的網頁，以及回應式設計的頁面，可根據裝置類型自動調整版面。

當檢視器在初始載入後未變更其大小時，會使用固定大小內嵌。 這是具有靜態版面的網頁的最佳選擇。

回應式設計內嵌假設檢視器可能需要在執行時期調整大小，以因應容器的大小變更 `DIV`。 最常見的使用案例是將檢視器新增至使用彈性頁面版面的網頁。

在回應式設計內嵌模式中，檢視器的運作方式視網頁大小容器而有所不同 `DIV`。 如果網頁只設定容器的寬度，而不限制其高度 `DIV`，檢視器會根據所使用資產的外觀比例自動選擇其高度。 此功能可確保資產完美整合至檢視中，而不會在側邊產生任何填補空間。 此使用案例是使用自適應版面架構（例如引導、基礎等）的網頁最常見的使用案例。

否則，如果網頁同時設定檢視器容器的寬度和高度 `DIV`，檢視器會填滿該區域，並遵循網頁版面所提供的大小。 一個很好的例子是將檢視器內嵌至模態覆蓋，其中覆蓋會根據網頁瀏覽器視窗大小而調整大小。

**固定大小內嵌**

您可執行下列動作，將檢視器新增至網頁：

1. 將檢視器JavaScript檔案新增至您的網頁。
1. 定義容器DIV。
1. 設定檢視器大小。
1. 建立和初始化檢視器。

1. 將檢視器JavaScript檔案新增至您的網頁。

   建立檢視器時，您必須在HTML標題中新增指令碼標籤。 在您使用檢視器API之前，請確定您已加入 [!DNL eCatalogSearchViewer.js]。 此檔 [!DNL eCatalogSearchViewer.js] 案位於標準IS- [!DNL html5/js/] Viewer部署的子資料夾下：

[!DNL <s7viewers_root>/html5/js/eCatalogSearchViewer.js]

如果檢視器部署在其中一個Adobe Scene7伺服器上，且是從相同網域提供，則可使用相對路徑。 否則，您會指定一個安裝IS-Viewer之Adobe Scene7伺服器的完整路徑。

相對路徑如下所示：

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/eCatalogSearchViewer.js"></script>
```

1. 定義容器DIV。

   將空的DIV元素新增至您要檢視器顯示的頁面。 DIV元素必須定義其ID，因為此ID稍後會傳遞至檢視器API。

   預留位置DIV是定位的元素，這表示 `position` CSS屬性已設為 `relative` 或 `absolute`。

   以下是已定義預留位置DIV元素的範例：

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. 設定檢視器大小

   您可以設定檢視器的靜態大小，方法是以絕對單位 `.s7ecatalogsearchviewer` 來宣告頂層CSS類別，或使用修飾 `stagesize` 元。

   您可以直接在HTML頁面上或自訂檢視器CSS檔案中放入CSS大小，然後將檔案指派給Scene7 Publishing System中的檢視器預設記錄，或使用樣式命令明確傳遞。

   如需 [使用CSS設定檢視器樣式的詳細資訊，請參閱自訂eCatalog檢視器](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) 。

   以下是在HTML頁面中定義靜態檢視器大小的範例：

   ```
   #s7viewer.s7ecatalogsearchviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   您可以在Scene7 Publishing System的檢視器預設記錄中設定修飾元，或以檢視器初始化程式碼與系列明確傳遞修飾元，或以「命令參考」區段中所述的API呼叫方式傳遞 `stagesize``params` ，如下所示：

   ```
   eCatalogSearchViewer.setParam("stagesize", 
   "640,480");
   ```

1. 初始化檢視器。

   完成上述步驟後，您將建立類的實例，將所有配置資訊 `s7viewers.eCatalogSearchViewer` 傳遞給其建構子，並在查看器實例 `init()` 上調用方法。 設定資訊會以JSON物件的形式傳遞至建構函式。 此物件至少會有欄位， `containerId` 其中包含檢視器容器ID名稱和內嵌 `params` JSON物件，以及檢視器支援的設定參數。 在此情況下，物 `params` 件必須至少將「影像伺服URL」傳遞為屬 `serverUrl` 性，並將初始資產傳遞為 `asset` 參數。 以JSON為基礎的初始化API可讓您使用單行程式碼來建立和啟動檢視器。

   請務必將檢視器容器新增至DOM，如此檢視器程式碼就能依其ID找到容器元素。 有些瀏覽器會延遲建立DOM，直到網頁結束為止。 不過，為獲得最大相容性，請 `init()` 在結束標籤之前或在 `BODY` body事件上呼叫方 `onload()` 法。

   同時，容器元素也不一定是網頁版面的一部分。 例如，它可能會使用指派給它 `display:none` 的樣式隱藏。 在此情況下，檢視器會延遲其初始化程式，直到網頁將容器元素帶回版面為止。 發生此情況時，檢視器載入會自動繼續。

   以下是建立檢視器例項、將最小必要的設定選項傳遞至建構函式，以及呼叫方法的范 `init()` 例。 範例假設 `eCatalogSearchViewer` 是檢視器例項； `s7viewer` 是佔位符的名稱 `DIV`; `http://s7d1.scene7.com/is/image/` 是影像伺服URL, `Viewers/Pluralist` 且是資產：

   ```
   <script type="text/javascript"> 
   var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "searchserverurl":"http://s7search1.scene7.com/s7search/" 
   } 
   }).init(); 
   </script>
   ```

   下列程式碼是內嵌固定大小之eCatalog Search檢視器之平凡網頁的完整範例：

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7ecatalogsearchviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "searchserverurl":"http://s7search1.scene7.com/s7search/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**不受高度限制的自適應設計內嵌**

有了互動式設計內嵌功能，網頁通常就有某種靈活的版面配置，可決定檢視器容器的執行時期大小 `DIV`。 在此範例中，假設網頁可讓檢視者的容器取用40%的網頁瀏 `DIV` 覽器視窗大小，而不會限制其高度。 產生的網頁HTML程式碼如下所示：

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

將檢視器新增至此類頁麵類似於固定大小內嵌，唯一的差異是您不需要明確定義檢視器大小。

1. 將檢視器JavaScript檔案新增至您的網頁。
1. 定義容器DIV。
1. 建立和初始化檢視器。

上述所有步驟都與固定大小內嵌相同。 將容器新 `DIV` 增至現有的「持有者」 `DIV`。 以下程式碼為完整範例。 您可以看到在調整瀏覽器大小時，檢視器大小的變更，以及檢視器外觀比例與資產的相符程度。

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
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
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "searchserverurl":"http://s7search1.scene7.com/s7search/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

下列範例頁面說明不受限制高度的互動式設計內嵌的實際使用案例：

[即時展示](https://landing.adobe.com/tw/na/dynamic-media/ctir-2755/live-demos.html)

**定義寬高的彈性大小內嵌**

若是定義了寬度和高度的彈性大小內嵌，網頁樣式會有所不同。 也就是說，它會為「持有者」提供兩種大小， `DIV` 並將它置於瀏覽器視窗中。 此外，網頁會將元素和元素的大 `HTML` 小設 `BODY` 為100%:

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

其餘的嵌入步驟與高度不受限制的自適應設計嵌入步驟相同。 產生的範例如下：

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
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
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "searchserverurl":"http://s7search1.scene7.com/s7search/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**使用Setter型API內嵌**

與其使用JSON型初始化，您可使用setter型API和no-args建構函式。 使用該API建構函式時，不會使用任何參數，而設定參數是使用 `setContainerId()`、 `setParam()``setAsset()` API方法以及個別的JavaScript呼叫來指定。

下列範例顯示使用setter-based API的固定大小內嵌：

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7ecatalogsearchviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer(); 
eCatalogSearchViewer.setContainerId("s7viewer"); 
eCatalogSearchViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
eCatalogSearchViewer.setParam("searchserverurl", "http://s7search1.scene7.com/s7search/"); 
eCatalogSearchViewer.setAsset("Viewers/Pluralist"); 
eCatalogSearchViewer.init(); 
</script> 
</body> 
</html>
```

