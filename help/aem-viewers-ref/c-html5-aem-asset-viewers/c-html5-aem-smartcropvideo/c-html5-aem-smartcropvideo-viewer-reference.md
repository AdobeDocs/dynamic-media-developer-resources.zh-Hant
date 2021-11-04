---
title: 智慧型裁切視訊
description: 智慧型裁切視訊檢視器是視訊播放器，除了新增智慧型裁切支援外，還會播放以H.264格式編碼的串流和漸進式視訊。 由Dynamic Media Classic或Adobe Experience Manager與Dynamic Media一起提供。
keywords: 回應式
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: null
source-git-commit: 254d1ef05c73e19618b7ad4743c6a242fa177929
workflow-type: tm+mt
source-wordcount: '2410'
ht-degree: 0%

---

# 視訊{#video}

智慧型裁切視訊檢視器是視訊播放器，除了新增智慧型裁切支援外，還會播放以H.264格式編碼的串流和漸進式視訊。 它是從Dynamic Media Classic或透過Dynamic MediaExperience Manager提供。

請參閱 [系統需求和先決條件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

支援單一視訊和最適化視訊集。 此外，檢視器支援使用裝載在外部位置的漸進式視訊和HLS資料流。 它專為支援HTML5視訊的案頭版和行動版網頁瀏覽器所設計。 此檢視器也支援視訊內容、視訊章節導覽和社交媒體分享工具頂端顯示的可選隱藏式字幕。

只要基礎系統支援，智慧型裁切視訊檢視器就會在其預設設定中使用HLS格式的HTML5串流視訊播放。 在不支援HTML5串流的系統上，檢視器會回復為HTML5漸進式視訊傳送。

檢視器類型518。

## 示範URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS](https://s7d9.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS)

## 使用智慧型裁切視訊檢視器 {#section-f21ac23d3f6449ad9765588d69584772}

智慧型裁切視訊檢視器代表主要JavaScript檔案和一組協助檔案 — 單一JavaScript包含所有檢視器SDK元件，供檢視器在執行階段下載的特定檢視器、資產和CSS使用。

您可以使用IS-Viewers隨附的生產就緒HTML頁面，以快顯模式使用智慧型裁切視訊檢視器。 或者，您可以在內嵌模式中使用檢視器，透過記錄的API將其整合至目標網頁。

設定檢視器和設定檢視器外觀的任務與其他檢視器類似。 所有外觀設定都是透過自訂CSS來達成。

請參閱 [所有檢視器通用的命令參考 — 設定屬性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 和 [所有檢視器 — URL通用的命令參考](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 與智慧型裁切視訊檢視器互動 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

智慧型裁切視訊檢視器提供一組用於視訊播放的標準使用者介面控制項，例如：

* 播放/暫停按鈕。
* 視頻清除器視頻時間泡泡。
* 播放時間/總時間指標。
* 音量控制。
* 全螢幕按鈕。
* 隱藏式字幕切換。

所有這些控制項都會分組到檢視器使用者介面底部的控制列中。

在觸摸設備上，音量控制在用戶介面中隱藏，因為只能使用硬體按鈕控制音量。

檢視器在快顯模式中運作時，使用者介面中無法使用全螢幕按鈕。

啟動視訊章節時，可快速導覽視訊內容。 視訊章節在視訊清除程式追蹤中顯示為標籤，並在滑鼠滑鼠變換或在觸控系統上點選一下時，顯示章節標題和相關說明。 使用者可以選取章節標籤或選取章節說明泡泡來尋找特定章節。

檢視器支援Windows裝置上的觸控輸入和滑鼠輸入，且具有觸控式螢幕和滑鼠。 不過，此支援僅限Chrome、Internet Explorer 11和Edge網頁瀏覽器。

此查看器可完全通過鍵盤訪問。

請參閱 [鍵盤協助工具和導覽](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## 使用智慧型裁切視訊檢視器的社交媒體分享工具 {#section-907d316fe1da4b87abb9775f02464704}

智慧型裁切視訊檢視器支援社交媒體分享工具。 使用者按一下或點選使用者介面中的單一按鈕，即可展開至共用工具列。

共用工具列包含支援之每種共用管道類型的圖示，例如Facebook、Twitter、電子郵件共用、內嵌程式碼共用和連結共用。 啟用電子郵件共用、內嵌共用或連結共用工具時，檢視器會顯示含有對應資料輸入表單的強制回應對話方塊。 呼叫Facebook或Twitter時，檢視器會將使用者重新導向至社交媒體服務的標準共用對話方塊。 共用工具啟動時，也會自動暫停視訊播放。

由於網頁瀏覽器安全性限制，無法以全螢幕模式使用共用工具。

## 內嵌智慧型裁切視訊檢視器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同的網頁對檢視者行為有不同的需求。 有時，網頁會提供連結，當選取時，連結會在個別瀏覽器視窗中開啟檢視器。 在其他情況下，則需直接將檢視器內嵌在托管頁面上。 在後一種情況下，網頁可能具有靜態頁面版面，或使用在不同裝置上或針對不同瀏覽器視窗大小顯示不同的回應式設計。 為了滿足這些需求，檢視器支援三種主要操作模式：快顯視窗、固定大小內嵌和回應式設計內嵌。

平板電腦和行動裝置支援在同一頁內嵌多個影片。 通常一次只能播放一個視訊。 當使用者開始播放一個視訊，然後嘗試播放另一個視訊時，第一個視訊會自動暫停。 自動暫停的視訊會記住目前的播放時間，因此使用者可以隨時回到該視訊並繼續播放。 此規則的唯一例外是Android™ 4.x裝置上的Chrome瀏覽器，可同時播放視訊。

**關於快顯模式**

在快顯模式中，檢視器會在個別的網頁瀏覽器視窗或標籤中開啟。 它會取用整個瀏覽器視窗區域，並在瀏覽器調整大小或裝置方向變更時進行調整。

此模式是行動裝置最常見的模式。 網頁會使用 `window.open()` JavaScript呼叫，已正確設定 `A` HTML元素，或任何其他合適的方法。

建議您對快顯操作模式使用現成可用的HTML頁面。 稱為 [!DNL SmartCropVideoViewer.html] 位於 [!DNL html5/] 標準IS — 檢視器部署的子資料夾：

[!DNL <s7viewers_root>/html5/SmartCropVideoViewer.html]

您可以套用自訂CSS來達到視覺化自訂。

以下是在新視窗中開啟檢視器的HTML程式碼範例：

```
<a href="http://s7d1.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS" target="_blank">Open popup viewer</a>
```

**關於固定大小內嵌模式和回應式內嵌模式**

在內嵌模式中，檢視器會新增至現有網頁，而現有網頁可能已有與檢視器無關的客戶內容。 瀏覽者通常只佔據網頁的一部分房地產。

主要使用案例是以桌上型電腦或平板電腦裝置為導向的網頁，以及可根據裝置類型自動調整版面的回應式設計頁面。

當檢視器在初始載入後未變更大小時，會使用固定大小內嵌。 此選項最適合具有靜態頁面配置的網頁。

回應式設計內嵌假設檢視器必須在執行階段中調整大小，以回應其容器的大小變更 `DIV`. 最常見的使用案例是將檢視器新增至使用彈性頁面版面的網頁。

在回應式設計內嵌模式中，檢視器的運作方式會因網頁大小其容器的方式而異 `DIV`. 如果網頁僅設定容器的寬度 `DIV`，而不限制其高度，則檢視器會根據所使用資產的外觀比例自動選取高度。 此方法可確保資產完全符合檢視，而無需在側邊填補。 此使用案例最常用於使用回應式設計配置架構(例如Bootstrap或Foundation)的網頁。

否則，如果網頁同時設定檢視器容器的寬度和高度 `DIV`，則檢視器會填入該區域，並遵循網頁版面所提供的大小。 一個很好的範例是將檢視器內嵌至強制回應覆蓋中，其中覆蓋會根據網頁瀏覽器視窗的大小而調整大小。

**固定大小嵌入**

您可以執行下列操作，將檢視器新增至網頁：

1. 將檢視器JavaScript檔案新增至您的網頁。
1. 定義容器 `DIV`.
1. 設定檢視器大小。
1. 建立和初始化檢視器。

1. 將檢視器JavaScript檔案新增至您的網頁。

   建立檢視器需要在HTML標題中新增指令碼標籤。 使用檢視器API之前，請務必加入 [!DNL SmartCropVideoViewer.js]. 此 [!DNL SmartCropVideoViewer.js] 檔案位於 [!DNL html5/js/] 標準IS — 檢視器部署的子資料夾：

[!DNL <s7viewers_root>/html5/js/SmartCropVideoViewer.js]

如果檢視器部署在其中一個Adobe Dynamic Media Classic伺服器上，且是從相同網域提供，則可使用相對路徑。 否則，您會指定安裝IS-Viewers之一Adobe Dynamic Media Classic伺服器的完整路徑。

相對路徑如下所示：

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/SmartCropVideoViewer.js"></script>
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

   確保全螢幕功能在Internet Explorer中正常運作。 確認DOM中沒有其他元素的堆疊順序比預留位置DIV高。

   以下是定義預留位置DIV元素的範例：

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. 設定檢視器大小

   您可以為聲明來設定檢視器的靜態大小 `.s7videoviewer` 以絕對單位表示的頂層CSS類，或使用修飾詞 `stagesize`.

   您可以直接在HTML頁面或自訂檢視器CSS檔案中放入CSS大小。 它稍後會指派給Dynamic Media Classic中的檢視器預設集記錄，或使用style命令明確傳遞。

   請參閱 [自訂智慧型裁切視訊檢視器](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e) 如需使用CSS來設定檢視器樣式的詳細資訊。

   以下是在HTML頁面中定義靜態檢視器大小的範例：

   ```
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   您可以設定 `stagesize` 修飾元(在Dynamic Media Classic的檢視器預設集記錄中)，或以檢視器初始化程式碼明確傳遞 `params` 集合。 或以API呼叫的形式（如命令參考區段所述），如下列所示：

   ```
   smartCropVideoViewer.setParam("stagesize", "640,480");
   ```

   建議使用CSS型方法，此範例中會使用。

1. 建立和初始化檢視器。

   完成上述步驟後，請建立例項 `s7viewers.SmartCropVideoViewer` 類，將所有配置資訊傳遞到其建構子，並調用 `init()` 方法。 設定資訊會以JSON物件的形式傳遞至建構函式。 至少，此物件應具有 `containerId` 欄位，其中包含檢視器容器ID和巢狀的名稱 `params` 檢視器支援之設定參數的JSON物件。 在這種情況下， `params` 物件至少必須以 `serverUrl` 屬性，傳遞的視訊伺服器URL為 `videoserverurl` 屬性，而初始資產為 `asset` 參數。 JSON型初始化API可讓您使用一行程式碼來建立和啟動檢視器。

   請務必將檢視器容器新增至DOM，讓檢視器程式碼可以透過其ID來尋找容器元素。 有些瀏覽器會延遲建立DOM，直到網頁結尾為止。 如需最大相容性，請呼叫 `init()` 方法 `BODY` 標籤，或在內文上 `onload()` 事件。

   同時，容器元素還不一定是網頁版面的一部分。 例如，您可能會使用 `display:none` 樣式。 在此情況下，檢視器會延遲其初始化程式，直到網頁將容器元素帶回版面的那一刻為止。 發生此動作時，檢視器載入會自動恢復。

   以下是建立檢視器例項、將最低必要設定選項傳遞至建構函式，並呼叫 `init()` 方法。 此範例假設 `smartCropVideoViewer` 是檢視器例項， `s7viewer` 是佔位符的名稱 `DIV`, [!DNL http://s7d1.scene7.com/is/image/] 是影像伺服URL, [!DNL http://s7d1.scene7.com/is/content/] 是視訊伺服器URL，且 [!DNL html5automation/frisbee-AVS] 是資產。

   ```
   <script type="text/javascript"> 
   var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"html5automation/frisbee-AVS", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   ```

   以下程式碼是嵌入大小固定的智慧型裁切視訊檢視器的簡單網頁的完整範例：

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   <script type="text/javascript"> 
   var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"html5automation/frisbee-AVS", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html> 
   ```

**無限制高度的回應式設計內嵌**

透過回應式設計內嵌，網頁通常會有某種彈性的版面配置，決定檢視器容器的執行時間大小 `DIV`. 針對此範例，假設網頁允許檢視者的容器 `DIV` 取用40%的網頁瀏覽器視窗大小，使其高度不受限制。 網頁HTML程式碼如下所示：

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

將檢視器新增至此類頁面，類似於固定大小的內嵌；唯一的差異是您不需要明確定義檢視器大小。

1. 將檢視器JavaScript檔案新增至您的網頁。
1. 定義容器DIV。
1. 建立和初始化檢視器。

上述所有步驟與固定大小嵌入相同。 新增容器 `DIV` 至現有「持有者」 `DIV`. 下列程式碼為完整的範例。 您可以查看瀏覽器調整大小時檢視器大小的變更，以及檢視器外觀比例與資產的相符情形。

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
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
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"html5automation/frisbee-AVS", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
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

其餘的嵌入步驟與高度不受限制的響應式設計嵌入相同。 產生的範例如下：

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
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
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"html5automation/frisbee-AVS", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7videoviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer(); 
smartCropVideoViewer.setContainerId("s7viewer"); 
smartCropVideoViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
smartCropVideoViewer.setParam("videoserverurl", "http://s7d1.scene7.com/is/content/"); 
smartCropVideoViewer.setAsset("html5automation/frisbee-AVS"); 
smartCropVideoViewer.init(); 
</script> 
</body> 
</html> 
```
