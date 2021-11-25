---
title: 全景檢視器
description: HTML5全景檢視器是顯示全景影像的影像檢視器。 此檢視器的目的是顯示球形全景圖，也稱為等矩形影像。 它支援通過陀螺運動自動平移和平移。  專為在桌上型電腦和行動裝置上運作而設計。  支援的行動裝置上提供虛擬現實檢視模式。
keywords: 回應式
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: null
source-git-commit: 959089682d432a72b1860f2180daac7de0afedf2
workflow-type: tm+mt
source-wordcount: '1961'
ht-degree: 0%

---

# 全景{#panoramic}

HTML5全景檢視器是顯示全景影像的影像檢視器。 此檢視器的目的是顯示球形全景圖，也稱為等矩形影像。 它支援通過陀螺運動自動平移和平移。  專為在桌上型電腦和行動裝置上運作而設計。  支援的行動裝置上提供虛擬現實檢視模式。

請參閱 [系統需求和先決條件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).


檢視器類型514。

## 示範URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample](http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample)

## 使用全景查看器 {#section-f21ac23d3f6449ad9765588d69584772}

HTML5全景檢視器代表檢視器在執行階段下載的主要JavaScript檔案和一組協助檔案(單一JavaScript包含此特定檢視器、資產、CSS所使用的所有HTML5檢視器SDK元件)。
HTML5全景檢視器可使用隨IS檢視器提供的生產就緒HTML頁面，或在內嵌模式中使用，透過記錄的API將其整合至目標網頁。
設定和外觀類似於其他HTML5檢視器。 所有外觀設定皆可透過自訂CSS來達成。

請參閱 [所有檢視器通用的命令參考 — 設定屬性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 和 [所有檢視器 — URL通用的命令參考](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 與HTML5全景檢視器互動 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

HTML5全景查看器支援通過拖動或陀螺移動自動平移和導航。

<table id="table_panoramic"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>導覽 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>桌上型電腦 </p> </td> 
   <td colname="col2"> <p>自動平移和拖曳以導覽。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>觸摸裝置 </p> </td> 
   <td colname="col2"> <p>依預設，自動平移和拖曳以導覽。 在VR轉譯模式中依迴旋式移動導覽(vrrender=true)。
 </p> </td> 
  </tr> 
 </tbody> 
</table>

檢視器在具有觸控螢幕和滑鼠的Windows裝置上，可同時支援觸控輸入和滑鼠輸入，但此支援僅限於Chrome、Internet Explorer 11和Edge網頁瀏覽器。
全景檢視器能夠透過指定vrrender修飾元，在虛擬現實(VR)模式中轉譯全景影像。  啟用vrrender時，全景影像會顯示在分割畫面中。  常見的使用案例是在安裝在虛擬現實頭戴式耳機中的行動電話中提供影像，為每隻眼睛提供單獨的影像。  觀看者將響應頭部的陀螺運動並導航通過影像。

## 嵌入HTML5全景查看器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同的網頁對檢視者行為有不同的需求。 有時網頁會提供連結，而按一下該連結時，檢視器就會在個別的瀏覽器視窗中開啟。 在其他情況下，可能需要將檢視器直接嵌入托管頁面。 在後一種情況下，網頁可能具有靜態版面，或是「回應式」，且在不同裝置上或針對不同瀏覽器視窗大小顯示不同。 為了滿足這些需求，檢視器支援三種主要操作模式：彈出式視窗、固定大小內嵌和回應式內嵌。

**關於快顯模式**

在快顯模式中，檢視器會在個別的網頁瀏覽器視窗或標籤中開啟。 它會佔用整個瀏覽器視窗區域，並在瀏覽器調整大小或裝置方向變更時進行調整。

此模式是行動裝置最常見的模式。 網頁會使用window.open()JavaScript呼叫、正確設定的HTML元素或任何其他適當的方式載入檢視器。

建議您對快顯操作模式使用現成可用的HTML頁面。 稱為 [!DNL PanoramicViewer.html] 位於 [!DNL html5/] 標準IS — 檢視器部署的子資料夾：

[!DNL <s7viewers_root>/html5/PanoramicViewer.html]

可透過套用自訂CSS來實現視覺化自訂。

以下是在新視窗中開啟檢視器的HTML程式碼範例：

```
<a href="http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample" target="_blank">Open popup viewer</a>
```

**關於固定大小內嵌模式和回應式內嵌模式**

在內嵌模式中，檢視器會新增至現有網頁，而現有網頁可能已有與檢視器無關的客戶內容。 觀看者通常只佔有網頁的一部分空間。

主要使用案例為以桌上型電腦或平板電腦裝置為導向的網頁，以及可根據裝置類型自動調整版面的回應式網頁。

當檢視器在初始載入後未變更大小時，會使用固定大小內嵌。 這是靜態版面的網頁最佳選擇。

回應式內嵌假設檢視器可能需要在執行時間調整大小，以回應其容器DIV的大小變更。 最常見的使用案例是在使用彈性版面的網頁中新增檢視器。

在回應模式中，檢視器的行為會因網頁大小其容器DIV的方式而異。 如果網頁僅設定容器DIV的寬度，保持高度不受限制，則檢視器會根據所使用的資產的外觀比例自動選擇其高度；這可確保資產完全符合檢視，而無需邊框上的邊框間距。 此使用案例是使用回應式版面架構(如Bootstrap、Foundation等)的網頁中最常見的使用案例。

否則，如果網頁同時設定檢視器容器DIV的寬度和高度，檢視器只會填入該區域，並遵循網頁版面所提供的大小。 一個很好的範例是將檢視器內嵌至強制回應覆蓋中，其中覆蓋會根據網頁瀏覽器視窗大小來調整大小。


**固定大小嵌入**

您可以執行下列操作，將檢視器新增至網頁：

1. 將檢視器JavaScript檔案新增至您的網頁。
1. 定義容器 `DIV`.
1. 設定檢視器大小。
1. 建立和初始化檢視器。

1. 將檢視器JavaScript檔案新增至您的網頁。

   建立檢視器需要在HTML標題中新增指令碼標籤。 使用檢視器API之前，請務必加入 [!DNL PanoramicViewer.js]. 此 [!DNL PanoramicViewer.js] 檔案位於 [!DNL html5/js/] 標準IS — 檢視器部署的子資料夾：

[!DNL <s7viewers_root>/html5/js/PanoramicViewer.js]

如果檢視器部署在其中一個Adobe Dynamic Media Classic伺服器上，且是從相同網域提供，則可使用相對路徑。 否則，您會指定安裝IS-Viewers之一Adobe Dynamic Media Classic伺服器的完整路徑。

相對路徑如下所示：

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/PanoramicViewer.js"></script>
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

   您可以為聲明來設定檢視器的靜態大小 `.s7panoramicviewer` 以絕對單位表示的頂層CSS類，或使用修飾詞 `stagesize`.

   CSS中的大小調整可以放在HTML頁面上，也可以放在自訂檢視器CSS檔案中，這些檔案稍後會指派給AOD中的檢視器預設集記錄，或使用style命令明確傳遞。 如需使用CSS來設定檢視器樣式的詳細資訊，請參閱自訂檢視器區段。 以下是在「HTML」頁面中定義靜態檢視器大小的範例：

   ```
   #s7viewer.s7panoramicviewer {
     width: 1024px;
     height: 512px;
   }
   ```

   `stagesize` 修飾元可與檢視器初始化程式碼搭配params集合明確傳遞，或如「命令參考」區段所述，以API呼叫的形式傳遞，如下所示：

   ```
   panoramicViewer.setParam("stagesize", "512,256");
   ```

   建議使用CSS型方法，此範例將會使用。


1. 建立和初始化檢視器。

   完成上述步驟後，請建立例項 `s7viewers.PanoramicViewer` 類，將所有配置資訊傳遞到其建構子並調用 `init(`)方法。 設定資訊會以JSON物件的形式傳遞至建構函式。 此物件至少應有containerId欄位，該欄位包含檢視器容器ID的名稱，以及檢視器支援的設定參數的巢狀參數JSON物件。 在此情況下，params物件必須至少將影像伺服URL傳遞為 `serverUrl` 屬性和初始資產。 JSON型初始化API可讓您使用一行程式碼來建立和啟動檢視器。

   請務必將檢視器容器新增至DOM，讓檢視器程式碼可以透過其ID來尋找容器元素。 有些瀏覽器會延遲建立DOM，直到網頁結尾為止。 如需最大相容性，請呼叫 `init()` 方法 `BODY` 標籤，或在內文上 `onload()` 事件。

   同時，容器元素還不一定是網頁版面的一部分。 例如，您可能會使用 `display:none` 樣式。 在此情況下，檢視器會延遲其初始化程式，直到網頁將容器元素帶回版面的那一刻為止。 發生此動作時，檢視器載入會自動恢復。

   以下是建立檢視器例項、將最低必要設定選項傳遞至建構函式，並呼叫 `init()` 方法。 此範例假設 `panoramicViewer` 是檢視器例項， `s7viewer` 是佔位符的名稱 `DIV`, [!DNL http://s7d1.scene7.com/is/image/] 是影像伺服URL，且 [!DNL Scene7SharedAssets/PanoramicImage-Sample] 是資產。

   ```
   <script type="text/javascript"> 
   var panoramicViewer = new s7viewers.PanoramicViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
     "asset":"Scene7SharedAssets/PanoramicImage-Sample",
     "serverurl":"http://s7d1.scene7.com/is/image/"
   } 
   }).init(); 
   </script> 
   ```

   以下代碼是嵌入具有固定大小的全景查看器的普通網頁的完整示例：

   ```
   <!DOCTYPE html> 
   <html> 
    <head>
    <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
    <style type="text/css">
    #s7viewer.s7panoramicviewer {
        width: 1024px;
        height: 512px;
    }
    </style>
    </head>
    <body>
    <div id="s7viewer" style="position:relative"></div>
    <script type="text/javascript">
    var panoramicViewer = new s7viewers.PanoramicViewer({
        "containerId":"s7viewer",
    "params":{
        "asset":"Scene7SharedAssets/PanoramicImage-Sample",
        "serverurl":"http://s7d1.scene7.com/is/image/"
    }
    }).init();
    </script>
    </body>
    </html>
   ```

**無限制高度的回應式設計內嵌**

透過回應式內嵌，網頁通常會有某種彈性的版面配置，這會指定檢視器容器DIV的執行時間大小。 在此範例中，我們假設網頁允許檢視器的容器DIV採用80%的網頁瀏覽器視窗大小，使其高度不受限制。 網頁HTML程式碼可能如下所示：

```
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
.holder {
	width: 80%;
}
</style>
</head>
<body>
<div class="holder"></div>
</body>
</html> 
```

將檢視器新增至此類頁面與固定大小內嵌非常類似，唯一的差異是您不需要明確定義檢視器大小：

1. 將檢視器JavaScript檔案新增至您的網頁。
1. 定義容器DIV。
1. 建立和初始化檢視器。

上述所有步驟與固定大小嵌入相同。 容器DIV應新增至現有的「保持器」DIV。 下列程式碼是完整的範例，您可能會看到瀏覽器調整大小時檢視器大小的變更，以及檢視器外觀比例與資產的相符情形。

```
<!DOCTYPE html>
<html>
<head>
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
<style type="text/css">
.holder {
	width: 80%;
}
</style>
</head>
<body>
<div class="holder">
<div id="s7viewer" style="position:relative"></div>
</div>
<script type="text/javascript">
var panoramicViewer = new s7viewers.PanoramicViewer({
	"containerId":"s7viewer",
"params":{
	"asset":"Scene7SharedAssets/PanoramicImage-Sample",
	"serverurl":"http://s7d1.scene7.com/is/image/"
}
}).init();
</script>
</body>
</html>
```

下列範例頁面說明在實際中更多使用高度不受限制的回應式設計內嵌：

[即時演示](https://landing.adobe.com/tw/na/dynamic-media/ctir-2755/live-demos.html)

[替代演示位置](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**定義寬度和高度的回應式設計內嵌**

如果定義了寬度和高度的回應式設計內嵌，則網頁樣式會有所不同；它為「保持器」提供了兩種大小 `DIV` 並在瀏覽器視窗中置入。 此外，網頁會設定 `HTML` 和 `BODY` 元素到100%:

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

其餘的嵌入步驟與高度不受限制的響應式嵌入相同。 結果範例為

```
<!DOCTYPE html>
<html>
<head>
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
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
var panoramicViewer = new s7viewers.PanoramicViewer({
	"containerId":"s7viewer",
"params":{
	"asset":"Scene7SharedAssets/PanoramicImage-Sample",
	"serverurl":"http://s7d1.scene7.com/is/image/"
}
}).init();
</script>
</body>
</html>
```

**使用基於Setter的API嵌入**

您可以使用setter型API和無目標建構函式，而不使用JSON型初始化。 使用該API時，建構函式不會取用任何參數，且會使用 `setContainerId()`, `setParam()`，和 `setAsset()` API方法搭配個別的JavaScript呼叫。

以下示例說明了使用基於setter的API進行固定大小嵌入：

```
<!DOCTYPE html>
<html>
<head>
<script language="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
<style type="text/css">
#s7viewer.s7panoramicviewer {
	width: 1024;
	height: 512;
}
</style>
</head>
<body>
<div id="s7viewer" style="position:relative"></div>
<script type="text/javascript">
var panoramicViewer = new s7viewers.PanoramicViewer();
panoramicViewer.setContainerId("s7viewer");
panoramicViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/");
panoramicViewer.setAsset("Scene7SharedAssets/PanoramicImage-Sample");
panoramicViewer.init();
</script>
</body>
</html>
```
