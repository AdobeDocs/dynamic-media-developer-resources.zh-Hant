---
description: 回轉檢視器是影像檢視器，可提供360度的影像檢視，或在使用適當的回轉集時提供多維檢視。 它提供縮放和旋轉工具、全螢幕支援，以及選購的關閉按鈕。 它可在桌上型電腦和行動裝置上運作。
keywords: 回應
solution: Experience Manager
title: Spin
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '2130'
ht-degree: 0%

---


# 迴轉{#spin}

回轉檢視器是影像檢視器，可提供360度的影像檢視，或在使用適當的回轉集時提供多維檢視。 它提供縮放和旋轉工具、全螢幕支援，以及選購的關閉按鈕。 它可在桌上型電腦和行動裝置上運作。

>[!NOTE]
>
>此檢視器不支援使用IR（影像演算）或UGC（使用者產生的內容）的影像。

檢視器類型503。

請參閱[系統需求和先決條件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

## 示範URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&amp;stagesize=500,400](https://s7d9.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&amp;stagesize=500,400)

## 使用回轉檢視器{#section-e6c68406ecdc4de781df182bbd8088b4}

回轉檢視器代表主要JavaScript檔案和一組輔助檔（單一JavaScript包含此特定檢視器使用的所有檢視器SDK元件、資產、CSS），由檢視器在執行時期下載。

回轉檢視器可使用隨附於IS檢視器的生產就緒HTML頁面，或在內嵌模式中，使用檔案化的API將回轉檢視器整合至目標網頁，以便在快顯模式中使用。

設定和外觀設定與其他檢視器類似。 所有外觀設定皆可透過自訂CSS完成。

請參閱所有檢視器通用的[命令參考——設定屬性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)和[所有檢視器通用的命令參考- URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 與回轉檢視器互動{#section-642e66ca38cd4032992840ec6c0b0cd2}

回轉檢視器支援下列觸控手勢，這些手勢在其他行動應用程式中很常見。 當檢視器無法處理使用者的滑動手勢時，會將事件轉送至網頁瀏覽器以執行原生頁面捲動。 這可讓使用者瀏覽頁面，即使檢視器佔據大部分裝置螢幕區域亦然。

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>手勢 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>按兩下 </p> </td> 
   <td colname="col2"> <p> 放大一個層級，直到達到放大率上限。 下一個點選手勢會將檢視器重設為初始檢視狀態。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>夾捏 </p> </td> 
   <td colname="col2"> <p>放大或縮小影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>水準滑動或輕拂 </p> </td> 
   <td colname="col2"> <p> 如果影像處於重設狀態，則會以水準方式旋轉設定。 </p> <p> 如果影像放大，則會水準移動影像。 如果影像移至檢視邊緣，而滑動仍朝該方向進行，手勢會執行原生頁面捲動。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直滑動或輕拂 </p> </td> 
   <td colname="col2"> <p> 如果影像處於重置狀態，則在使用多維旋轉集時，它會更改垂直視角。 在一維回轉集中，或當多維回轉集位於最後一個或第一軸上時，使垂直滑動不會導致垂直檢視角度改變，手勢會執行原生頁面捲動。 </p> <p> 如果影像放大，則會垂直移動影像。 如果影像移至檢視邊緣，而滑動仍朝該方向進行，手勢會執行原生頁面捲動。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>檢視器也支援觸控式螢幕和滑鼠的Windows裝置上的觸控輸入和滑鼠輸入。 不過，這項支援僅限Chrome、Internet Explorer 11和Edge網頁瀏覽器。

此檢視器可完全透過鍵盤存取。

請參閱[鍵盤協助功能和導覽](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 內嵌回轉檢視器{#section-6bb5d3c502544ad18a58eafe12a13435}

不同的網頁對檢視器行為有不同的需求。 有時網頁會提供連結，當點按時，會在個別的瀏覽器視窗中開啟檢視器。 在其他情況下，必須直接將檢視器內嵌在代管頁面中。 在後一種情況下，網頁可能具有靜態頁面版面，或使用不同裝置或不同瀏覽器視窗大小顯示不同的互動式設計。 為滿足這些需求，檢視器支援三種主要作業模式：快顯功能、固定大小內嵌和回應式設計內嵌。

**關於彈出式模式**

在快顯模式中，檢視器會在個別的網頁瀏覽器視窗或標籤中開啟。 它會佔用整個瀏覽器視窗區域，並在瀏覽器調整大小或行動裝置的方向變更時進行調整。

快顯模式是行動裝置最常見的模式。 網頁會使用`window.open()` JavaScript呼叫、正確設定的`A` HTML元素或任何其他適當的方法載入檢視器。

建議您使用現成可用的HTML頁面來進行快顯作業模式。 在此例中，它稱為[!DNL SpinViewer.html]，位於標準IS-Viewer部署的[!DNL html5/]子資料夾中：

[!DNL <s7viewers_root>/html5/SpinViewer.html]

您可以套用自訂CSS，以實現視覺化自訂。

以下是在新視窗中開啟檢視器的HTML程式碼範例：

```
<a 
href="http://s7d1.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&stagesize=500,400" 
target="_blank">Open popup viewer</a>
```

**關於固定大小嵌入模式和自適應設計嵌入模式**

在內嵌模式中，檢視器會新增至現有的網頁，而現有網頁可能已有與檢視器無關的客戶內容。 檢視器通常只佔用網頁的部分空間。

主要使用案例是針對桌上型電腦或平板電腦裝置的網頁，以及可根據裝置類型自動調整版面的自適應設計頁面。

當檢視器在初始載入後未變更其大小時，會使用固定大小內嵌。 這是具有靜態版面的網頁的最佳選擇。

回應式設計內嵌假設檢視器可能需要在執行時期調整大小，以回應其容器`DIV`的大小變更。 最常見的使用案例是將檢視器新增至使用彈性頁面版面的網頁。

在回應式設計內嵌模式中，檢視器的運作方式會因網頁大小的容器`DIV`而異。 如果網頁僅設定容器的寬度`DIV`，而不限制其高度，檢視器會根據所使用資產的寬高比自動選擇其高度。 此功能可確保資產完美整合至檢視中，而不會在側邊產生任何填補空間。 此使用案例是使用自適應設計版面架構(例如Bootstrap、基礎等)的網頁最常見的使用案例。

否則，如果網頁同時設定檢視器容器`DIV`的寬度和高度，檢視器只會填滿該區域，並遵循網頁版面所提供的大小。 一個很好的例子是將檢視器內嵌至模態覆蓋，其中覆蓋會根據網頁瀏覽器視窗大小而調整大小。

**固定大小內嵌**

您可執行下列動作，將回轉檢視器新增至網頁：

1. 將檢視器JavaScript檔案新增至您的網頁。
1. 定義容器`DIV`。
1. 設定檢視器大小。
1. 建立和初始化檢視器。

1. 將檢視器JavaScript檔案新增至您的網頁。

   建立檢視器時，您必須在HTML標題中新增指令碼標籤。 請務必加入`SpinViewer.js`，才能使用檢視器API。 `SpinViewer.js` 位於標準IS- [!DNL html5/js/] Viewer部署的子資料夾下：

   `<s7viewers_root>/html5/js/SpinViewer.js`

   如果檢視器部署在其中一個Adobe的Dynamic Media伺服器上，且是從相同網域提供，則可使用相對路徑。 否則，您將指定到安裝IS-Viewer的AdobeDynamic Media伺服器之一的完整路徑。

   相對路徑如下所示：

   ```
    <script language="javascript" type="text/javascript" src="/s7viewers/html5/js/SpinViewer.js"></script>
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

   以下是已定義預留位置DIV元素的範例：

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. 設定檢視器大小

   您可以設定檢視器的靜態大小，方法是以絕對單位聲明`.s7spinviewer`頂層CSS類別，或使用`stagesize`修飾元。

   您可以直接在HTML頁面上或自訂檢視器CSS檔案中放入CSS大小，然後再將檔案指派給Dynamic Media經典中的檢視器預設集記錄，或使用樣式命令明確傳遞。

   如需使用CSS設定檢視器樣式的詳細資訊，請參閱[自訂回轉檢視器](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-customizingviewer/c-html5-spin-viewer-customizingviewer.md#concept-464f3bfa55764bc09c92d8c7480b0b55)。

   以下是在HTML頁面中定義靜態檢視器大小的範例：

   ```
   #s7viewer.s7spinviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   您可以在Dynamic MediaClassic的檢視器預設記錄中設定`stagesize`修飾元，或以`params`系列的檢視器初始化程式碼明確傳遞它，或以「命令參考」區段中所述的API呼叫傳遞，如下所示：

   ```
    spinViewer.setParam("stagesize", 
   "640,480");
   ```

   建議使用以CSS為基礎的方法，並在此範例中使用。

1. 建立和初始化檢視器。

   完成上述步驟後，您將建立一個`s7viewers.SpinViewer`類的實例，將所有配置資訊傳遞給其建構子，並在查看器實例上調用`init()`方法。 設定資訊會以JSON物件的形式傳遞至建構函式。 此物件至少具有`containerId`欄位，其中包含檢視器容器ID的名稱，並以檢視器支援的組態參數巢狀內嵌`params` JSON物件。 在`params`物件的情況下，它至少必須將影像伺服URL傳遞為`serverUrl`屬性，並將初始資產傳遞為`asset`參數。 以JSON為基礎的初始化API可讓您使用單行程式碼來建立和啟動檢視器。

   請務必將檢視器容器新增至DOM，如此檢視器程式碼就能依其ID找到容器元素。 有些瀏覽器會延遲建立DOM，直到網頁結束為止。 為獲得最大相容性，請在`BODY`結束標籤之前或在主體`onload()`事件上調用`init()`方法。

   同時，容器元素也不一定是網頁版面的一部分。 例如，它可能會使用指派給它的`display:none`樣式進行隱藏。 在此情況下，檢視器會延遲其初始化程式，直到網頁將容器元素帶回版面為止。 發生此動作時，檢視器載入會自動繼續。

   以下是建立檢視器例項的範例，將最小必要的設定選項傳遞至建構函式並呼叫`init()`方法。 範例假設`spinViewer`是檢視器例項，`s7viewer`是預留位置`DIV`的名稱，[!DNL http://s7d1.scene7.com/is/image/]是影像伺服URL，而[!DNL Scene7SharedAssets/SpinSet_Sample]是資產。

   ```
   <script type="text/javascript"> 
   var spinViewer = new s7viewers.SpinViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/SpinSet_Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   以下程式碼是內嵌固定大小回轉檢視器之平凡網頁的完整範例：

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7spinviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var spinViewer = new s7viewers.SpinViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/SpinSet_Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**不受高度限制的自適應設計內嵌**

有了互動式設計內嵌功能，網頁通常就有某種靈活的版面配置，指定檢視器容器`DIV`的執行時期大小。 在此範例中，假設網頁允許檢視器的容器`DIV`取用40%的網頁瀏覽器視窗大小，並保留其高度不受限制。 產生的網頁HTML程式碼如下所示：

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

上述所有步驟都與固定大小內嵌相同。 將容器`DIV`新增至現有的&quot; holder&quot; `DIV`。 以下程式碼為完整範例。 您可以看到在調整瀏覽器大小時，檢視器大小的變更，以及檢視器外觀比例與資產的相符程度。

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
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
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

下列範例頁面說明不受限制高度的互動式設計內嵌的實際使用案例：

[即時展示](https://landing.adobe.com/tw/na/dynamic-media/ctir-2755/live-demos.html)

<!-- KEEP (https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html) -->

**定義寬高的彈性大小內嵌**

若是定義了寬度和高度的彈性大小內嵌，網頁樣式會有所不同。 也就是說，它會為&quot;holder&quot; `DIV`提供兩種大小，並將它們置於瀏覽器視窗中。 此外，網頁還將`HTML`和`BODY`元素的大小設為100%:

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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
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
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**使用Setter型API進行內嵌**

與其使用JSON型初始化，您可使用setter型API和no-args建構函式。 使用該API建構函式時，不會使用任何參數，而設定參數是使用`setContainerId()`、`setParam()`和`setAsset()` API方法，並使用個別的JavaScript呼叫來指定。

下列範例顯示使用setter-based API的固定大小內嵌：

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7spinviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var spinViewer = new s7viewers.SpinViewer(); 
spinViewer.setContainerId("s7viewer"); 
spinViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
spinViewer.setAsset("Scene7SharedAssets/SpinSet_Sample"); 
spinViewer.init(); 
</script> 
</body> 
</html>
```

