---
title: 全景檢視器
description: HTML5 Panoramic Viewer是顯示全景影像的影像檢視器。 此檢視器的目的是顯示球面全景，也稱為等矩形影像。 它支援透過迴轉運動自動平移和平移。 專為桌上型電腦和行動裝置所設計。 支援行動裝置的虛擬實境檢視模式可供使用。
keywords: 回應式
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: baf8015dc93cfa6be0a841243a7e3524f06f1639
workflow-type: tm+mt
source-wordcount: '1920'
ht-degree: 0%

---

# 全景{#panoramic}

HTML5 Panoramic Viewer是顯示全景影像的影像檢視器。 此檢視器的目的是顯示球面全景，也稱為等矩形影像。 它支援透過迴轉運動自動平移和平移。 專為桌上型電腦和行動裝置所設計。 支援行動裝置的虛擬實境檢視模式可供使用。

請參閱[系統需求和先決條件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。


檢視器型別514。

<!--
## Demo URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample](http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample)
-->

## 使用全景檢視器 {#section-f21ac23d3f6449ad9765588d69584772}

HTML5 Panoramic Viewer代表主要JavaScript檔案和一組協助程式檔案，由檢視器在執行階段下載。 這組協助程式檔案是單一JavaScript包含，以及此特定檢視器、資產、CSS使用的所有HTML5 Viewer SDK元件。
HTML5 Panoramic Viewer既可透過隨IS-Viewers提供的生產就緒HTML頁面以快顯模式使用，也可透過內嵌模式使用，其中使用記錄的API將其整合至目標網頁。
組態和外觀設定與其他HTML5檢視器的組態和外觀設定類似。 所有外觀設定均可以透過自訂CSS來達成。

檢視所有檢視器通用的[命令參考 — 組態屬性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)和所有檢視器通用的[命令參考 — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 與HTML5全景檢視器互動 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

HTML5 Panoramic Viewer支援透過拖曳或迴轉運動自動平移和導覽。

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
   <td colname="col1"> <p>觸控裝置 </p> </td> 
   <td colname="col2"> <p>依預設，自動平移和拖曳以導覽。 在VR轉譯器模式中透過迴轉運動導覽(vrrender=true)。
 </p> </td> 
  </tr> 
 </tbody> 
</table>

該檢視器在具有觸控熒幕和滑鼠的Windows裝置上支援觸控輸入和滑鼠輸入，但是這項支援僅限Chrome、Internet Explorer 11和Edge網頁瀏覽器。
全景檢視器可以透過指定vrrender修飾元在Virtual Reality (VR)模式中轉譯全景影像。 啟用vrrender時，全景影像會顯示在分割畫面中。 最常見的使用案例是透過掛載於虛擬現實頭戴式耳機的行動電話提供影像，為每隻眼睛提供個別影像。 檢視器會回應頭部的迴轉運動，並導覽整個影像。

## 內嵌HTML5全景檢視器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同的網頁對檢視者的行為有不同的需求。 有時網頁會提供連結。 選取該連結會在單獨的瀏覽器視窗中開啟檢視器。 在其他情況下，可能必須將檢視器內嵌在託管頁面中。 在後一種情況下，網頁可能具有靜態佈局，或「回應式」並在不同裝置或不同瀏覽器視窗大小上以不同方式顯示。 為因應這些需求，檢視器支援三種主要操作模式：快顯視窗、固定大小內嵌和回應式內嵌。

**關於快顯視窗模式**

在快顯視窗模式中，檢視器會在個別的網頁瀏覽器視窗或標籤中開啟。 它會取用整個瀏覽器視窗區域，並在瀏覽器調整大小或裝置方向變更時進行調整。

此模式在行動裝置中最常見。 網頁會使用`window.open()` JavaScript呼叫、正確設定的A HTML元素或任何其他合適的方式，載入檢視器。

建議您為快顯視窗操作模式使用現成可用的HTML頁面。 它稱為[!DNL PanoramicViewer.html]，且位於標準IS-Viewers部署的[!DNL html5/]子資料夾下：

[!DNL <s7viewers_root>/html5/PanoramicViewer.html]

可套用自訂CSS以達成視覺化自訂。

以下是在新視窗中開啟檢視器的HTML程式碼範例：

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample" target="_blank">Open popup viewer</a>
```

**關於固定大小內嵌模式和回應式內嵌模式**

在內嵌模式中，檢視器會新增至現有網頁，其中可能已有某些與檢視器無關的客戶內容。 檢視器通常只佔用網頁不動產的一部分。

主要使用案例是桌上型電腦或平板電腦裝置導向的網頁，以及可依裝置型別自動調整版面的回應式網頁。

當檢視器在初始載入後未變更其大小時，會使用固定大小內嵌。 此方法適用於具有靜態配置的網頁。

回應式內嵌假設檢視器必須在執行階段調整大小來回應其容器DIV的大小變更。 最常見的使用案例是將檢視器新增到使用彈性配置的網頁。

在回應模式中，檢視器的行為會因網頁調整其容器DIV大小的方式而異。 如果網頁僅設定容器DIV的寬度，並保持其高度不受限制，檢視器會根據所使用資產的外觀比例自動選擇其高度。 此方法可確保資產完全符合檢視方式，而不會在兩側加上任何邊框間距。 此使用案例最常用於使用回應式佈局架構(例如Bootstrap、Foundation等)的網頁。

否則，如果網頁同時設定檢視器容器DIV的寬度和高度，則檢視器會填滿該區域，並遵循網頁版面配置所提供的大小。 一個很好的範例是內嵌檢視器至強制回應覆蓋圖，其中覆蓋圖會根據網頁瀏覽器視窗大小調整大小。

**固定大小內嵌**

您可以執行下列動作，將檢視器新增至網頁：

1. 正在將viewer JavaScript檔案新增至您的網頁。
1. 定義容器`DIV`。
1. 設定檢視器大小。
1. 正在建立和初始化檢視器。

1. 正在將viewer JavaScript檔案新增至您的網頁。

   建立檢視器需要您在HTML標題中新增指令碼標籤。 在可以使用檢視器API之前，請確定您已包含[!DNL PanoramicViewer.js]。 [!DNL PanoramicViewer.js]檔案位於標準IS-Viewers部署的[!DNL html5/js/]子資料夾下：

[!DNL <s7viewers_root>/html5/js/PanoramicViewer.js]

如果檢視器部署在任一Adobe Dynamic Media Classic伺服器上，且從相同網域提供服務，您就可以使用相對路徑。 否則，請指定已安裝IS-Viewers之其中一個Adobe Dynamic Media Classic伺服器的完整路徑。

相對路徑如下所示：

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/PanoramicViewer.js"></script>
```

>[!NOTE]
>
>僅參考頁面上的主要檢視器JavaScript `include`檔案。 請勿在網頁程式碼中參考任何其他JavaScript檔案（這些檔案可能由執行階段的檢視器邏輯下載）。 特別是，請勿直接參考檢視器從`Utils.js`內容路徑(所謂整合的HTML `/s7viewers`)載入的SDK5 SDK `include`資料庫。 原因在於`Utils.js`或類似的執行階段檢視器程式庫的位置完全由檢視器的邏輯管理，且位置會在檢視器發行版本之間變更。 Adobe不會在伺服器上保留舊版的次要檢視器`includes`。
>
>
>因此，日後部署新產品版本時，將檢視器使用的任何次要JavaScript `include`的直接參照放在頁面上，會中斷檢視器功能。

1. 定義容器DIV。

   新增空的DIV元素至要顯示檢視器的頁面。 DIV元素必須定義其ID，因為此ID稍後會傳遞至檢視器API。 DIV的大小是透過CSS指定。

   預留位置DIV是定位元素，表示`position` CSS屬性設定為`relative`或`absolute`。


   以下為已定義預留位置DIV元素的範例：

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. 設定檢視器大小

   您可以透過以絕對單位宣告`.s7panoramicviewer`最上層CSS類別的檢視器，或使用修飾元`stagesize`來設定檢視器的靜態大小。

   CSS的大小調整可直接放在HTML頁面或自訂檢視器CSS檔案中，檔案稍後會指派給AOD中的檢視器預設集記錄，或是使用樣式命令明確傳遞。 如需使用CSS設定檢視器樣式的詳細資訊，請參閱自訂檢視器區段。 以下是在HTML頁面中定義靜態檢視器大小的範例：

   ```html {.line-numbers}
   #s7viewer.s7panoramicviewer {
     width: 1024px;
     height: 512px;
   }
   ```

   `stagesize`修飾元可透過params集合以檢視器初始化程式碼明確傳遞，或作為API呼叫傳遞，如Command Reference一節中所述，如下所示：

   ```html {.line-numbers}
   panoramicViewer.setParam("stagesize", "512,256");
   ```

   此範例中建議並使用以CSS為基礎的方法。

1. 正在建立和初始化檢視器。

   完成上述步驟後，您會建立`s7viewers.PanoramicViewer`類別的執行個體、將所有組態資訊傳遞至其建構函式，並在檢視器執行個體上呼叫`init(`)方法。 組態資訊會以JSON物件的形式傳遞至建構函式。 此物件至少應有containerId欄位，用以儲存檢視器容器ID和巢狀引數JSON物件的名稱，以及檢視器支援的設定引數。 在此情況下，params物件必須至少將影像伺服URL作為`serverUrl`屬性傳遞，並將初始資產作為資產引數傳遞。 JSON型初始化API可讓您使用一行程式碼來建立和啟動檢視器。

   請務必將檢視器容器新增至DOM，讓檢視器程式碼可依其ID尋找容器元素。 有些瀏覽器會延遲建立DOM，直到網頁結尾為止。 為達到最大相容性，請在結尾的`init()`標籤前面或內文`BODY`事件上呼叫`onload()`方法。

   同時，容器元素也不一定屬於網頁版面配置的一部分。 例如，可以使用指派給它的`display:none`樣式來隱藏它。 在此情況下，檢視器會延遲其初始化程式，直到網頁將容器元素帶回版面配置為止。 當此動作發生時，檢視器載入會自動繼續。

   以下是建立檢視器執行個體、將最低必要組態選項傳遞給建構函式，以及呼叫`init()`方法的範例。 此範例假設`panoramicViewer`為檢視器執行個體，`s7viewer`為預留位置名稱`DIV`，[!DNL http://s7d1.scene7.com/is/image/]為影像伺服URL，而[!DNL Scene7SharedAssets/PanoramicImage-Sample]為資產。

   ```html {.line-numbers}
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

   下列程式碼是嵌入固定大小全景檢視器的簡單網頁的完整範例：

   ```html {.line-numbers}
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

**高度不受限制的回應式設計內嵌**

透過回應式內嵌，網頁通常會有某種彈性的版面配置，可指定檢視器容器DIV的執行階段大小。 在此範例中，假設網頁允許檢視器的容器DIV佔據網頁瀏覽器視窗大小的80%，其高度不受限制。 HTML程式碼的網頁可能如下所示：

```html {.line-numbers}
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

將檢視器新增至這類頁面類似於內嵌固定大小，唯一差異是您不需要明確定義檢視器大小：

1. 正在將viewer JavaScript檔案新增至您的網頁。
1. 定義容器DIV。
1. 正在建立和初始化檢視器。

上述所有步驟與內嵌固定大小相同。 容器DIV應新增至現有的「持有者」DIV。 下列程式碼是完整的範例，您可能會看到瀏覽器調整大小時檢視器大小如何變更，以及檢視器外觀比例如何與資產相符。

```html {.line-numbers}
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

以下範例頁面說明高度不受限制的回應式設計內嵌在實際應用中的更多效果：

[即時示範](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[備用示範位置](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html?lang=zh-Hant)

**定義寬度和高度的回應式設計內嵌**

如果有已定義寬度和高度的回應式設計內嵌，則網頁樣式會不同；它會將「`DIV`」的大小提供給「托架」，並將它置中在瀏覽器視窗中。 此外，網頁會將`HTML`和`BODY`專案的大小設定為100%：

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

其餘的嵌入步驟與高度不受限制的回應式嵌入相同。 產生的範例是

```html {.line-numbers}
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

**使用Setter型API進行內嵌**

除了使用JSON型初始化之外，也可以使用setter型API和no-args建構函式。 使用該API，建構函式不會接受任何引數，而且設定引數是使用`setContainerId()`、`setParam()`和`setAsset()` API方法搭配個別的JavaScript呼叫所指定。

下列範例說明使用setter型API嵌入固定大小的內容：

```html {.line-numbers}
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
