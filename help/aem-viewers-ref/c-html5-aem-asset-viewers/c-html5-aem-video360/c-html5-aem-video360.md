---
title: 視頻360
description: HTML5 Video360 Viewer是360度視頻播放器，播放以H.264格式編碼的流媒體和漸進式360視頻，從Dynamic Media Classic或Dynamic MediaAdobe Experience Manager傳送。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 74dca3f6-ce89-4c5b-8459-c2c4ca8ed27c
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2569'
ht-degree: 0%

---

# 視頻360{#video}

HTML5 Video360 Viewer是360度視頻播放器，播放以H.264格式編碼的流媒體和漸進式360視頻，從Dynamic Media Classic或Dynamic MediaAdobe Experience Manager傳送。

360度視頻，又稱沈浸式視頻或球形視頻，是一些視頻錄制，在這些錄像中，可以同時記錄每個方向的視圖，使用全向攝像機或攝像機集合進行拍攝。 同時支援單個視頻和自適應視頻集。 該查看器還支援使用在外部位置承載的漸進式視頻和HLS流。

360視頻的建議寬高比為2:1。 不支援空間聲音。 觀看者設計為僅能處理360個視頻；試圖播放非360視頻會導致視頻回放失真。

該查看器設計用於支援HTML5視頻的案頭和移動Web瀏覽器。 查看器支援可選的社交共用工具。

Video360 Viewer在基礎系統支援時使用HLS格式的HTML5流視頻回放，其預設配置為。 在不支援HTML5流式傳輸的系統上，查看器將返回HTML5逐步視頻傳輸。

查看器類型為517。

## 演示URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS](https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS)

## 系統要求 {#section-b7270cc4290043399681dc504f043609}

請參閱 [系統要求](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

## 使用Video360查看器 {#section-e6c68406ecdc4de781df182bbd8088b4}

HTML5 Video360 Viewer表示主JavaScript檔案和一組幫助程式檔案(單個JavaScript包含此查看器、資產、CSS使用的所有HTML5 Viewer SDK元件)，該查看器在運行時下載。

HTML5 Video360 Viewer可以在彈出模式下使用隨IS-Viewer提供的生產就緒HTML頁，也可以在嵌入式模式下使用文檔化的API將其整合到目標網頁中。

配置和外觀與本指南中描述的其他查看器的配置和外觀相似。 所有蒙皮都通過自定義(CSS)層疊樣式表實現。

請參閱 [所有查看器通用的命令引用 — 配置屬性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 和 [所有查看器通用的命令引用 — URL](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-cmdref-url/c-html5-aem-video360-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

360視頻內容要求比標準非360視頻更高的編碼設定。 換句話說，360個內容必須比非360視頻的解析度更高才能達到相同的可感知質量。 建議您考慮360視頻的以下自適應視頻預設設定：

* 720p 、 2500 kbps
* 1080p, 5000 kbps
* 1440p 、 6600 kbps

但請注意，使用如此高質量設定編碼的視頻服務需要在最終用戶設備上進行高頻寬連接。

## 與Video360查看器交互 {#section-642e66ca38cd4032992840ec6c0b0cd2}

HTML5 Video360 Viewer提供一組用於視頻播放的標準用戶介面控制項，如播放/暫停按鈕、視頻掃描器視頻時間氣泡、播放時間/總時間指示器、音量控制和全屏按鈕。 所有這些控制項都分組到查看器用戶介面底部的控制欄中。

在觸摸設備上，卷控制項被隱藏在用戶介面之外，因為只能使用設備的硬體按鈕來控制卷。

當查看器在彈出模式下操作時，用戶介面中不提供全屏按鈕。

觀眾還支援各種社交媒體共用工具。 它們可作為用戶介面中的單個按鈕使用，當用戶按一下或輕擊該按鈕時，該按鈕會擴展到共用工具欄。 共用工具欄包含支援的每種類型的共用通道的表徵圖，如Facebook、Twitter、電子郵件共用、嵌入代碼共用和連結共用。 當激活電子郵件共用、嵌入共用或連結共用工具時，查看器將顯示帶有相應資料輸入表單的模式對話框。 當呼叫Facebook或Twitter時，觀看者將用戶從社交媒體服務重定向到標準共用對話框。 此外，當共用工具被激活時，視頻回放將自動暫停。 由於Web瀏覽器安全限制，共用工具在全屏模式下不可用。

查看器支援以下360個視頻播放：

* VR耳機(如OculusGo和OculusRift)
* VR HMD（頭戴式顯示器）支架(如Google紙板)
* 未啟用VR的設備（如未連接到VR HMD安裝的案頭瀏覽器、平板電腦和行動電話）

在VR頭戴式耳機上查看360個視頻內容無需其他配置。 觀看者自動檢測VR頭戴式耳機的存在，並在視頻內容的頂部顯示「VR」按鈕。 激活此「VR」按鈕可將視頻呈現切換為VR模式。 僅在支援WebVR的瀏覽器中，查看器才支援VR呈現。

為了使用VR HMD裝載 `Video360Player.vrrender` 修飾符必須設定為 `1` 在觀看者配置中，強制進行立體渲染。

在VR耳機和VR HMD安裝上，視點變化會響應於頭戴式耳機移動而發生，而不是在VR模式中提供其它回放控制。

在啟用非VR的設備上觀看360個視頻時，最終用戶可以使用滑鼠、觸摸或鍵盤來控制視頻播放和視點。

查看器支援Windows設備上的觸摸輸入和滑鼠輸入，並帶有觸摸屏和滑鼠，但僅限於Chrome、Internet Explorer 11和Edge Web瀏覽器。

可以完全使用鍵盤訪問查看器。 請參閱 [鍵盤輔助功能和導航](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 嵌入Video360查看器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同的網頁對查看者行為有不同的需求。 有時，網頁提供的連結在選中時會在單獨的瀏覽器窗口中開啟查看器。 在其他情況下，必須將查看器直接嵌入到托管頁面中。 在後一種情況下，該網頁可以具有靜態頁面佈局，或者使用響應設計，該響應設計在不同的設備上顯示不同的或針對不同的瀏覽器窗口大小。 為滿足這些需要，查看器支援三種主要操作模式：彈出式、固定大小嵌入和響應性設計嵌入。

平板電腦和移動設備支援在同一頁面上嵌入多個視頻。 通常，一次只能播放一個視頻。 當用戶開始播放一個視頻，然後嘗試播放另一個視頻時，第一個視頻將自動暫停。 自動暫停的視頻會記住其當前的播放時間，因此用戶可以始終返回到它並繼續播放。 此規則唯一的例外是Android™ 4.x設備上的Chrome瀏覽器，該瀏覽器可以並行播放視頻。

**關於彈出模式**

在彈出模式下，在單獨的Web瀏覽器窗口或頁籤中開啟查看器。 它會佔用整個瀏覽器窗口區域，並在瀏覽器調整大小或設備方向發生變化時進行調整。

此模式是移動設備中最常見的模式。 網頁使用 `window.open()` JavaScript調用，正確配置 `A` HTML元件或任何其它合適的方法。

建議您使用現成HTML頁面進行彈出操作模式。 它叫 [!DNL Video360Viewer.html] 它位於 [!DNL html5/] 標準IS查看器部署的子資料夾：

[!DNL <s7viewers_root>/html5/Video360Viewer.html]

通過應用自定義CSS，可以實現可視化定製。

以下是在新窗口中開啟查看器的HTML代碼示例：

```html {.line-numbers}
<a href="https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS" target="_blank">Open popup viewer</a>
```

**關於固定尺寸嵌入模式和響應設計嵌入模式**

在嵌入模式中，查看器被添加到現有網頁中，該網頁可能已經具有與查看器無關的一些客戶內容。 瀏覽者通常只佔用網頁的一部分房地產。

主要使用案例是面向台式機或平板電腦設備的網頁，以及響應性設計的頁面，這些頁面根據設備類型自動調整佈局。

當查看器在初始載入後不更改其大小時，使用固定大小嵌入。 此方法是具有靜態佈局的網頁的最佳選擇。

響應性設計嵌入假定查看器必須在運行時根據其容器的大小變化調整大小 `DIV`。 最常見的用例是向使用靈活頁面佈局的網頁添加查看器。

在響應性設計嵌入模式中，查看器根據網頁大小其容器的方式而具有不同的行為 `DIV`。 如果網頁僅設定容器的寬度 `DIV`在保持高度不受限制的情況下，觀看者根據所使用資產的縱橫比自動選擇其高度。 此功能可確保資產完美地貼入視圖中，而不會在側面出現任何填充。 此使用案例是使用響應性Web設計佈局框架(如Bootstrap和Foundation)的Web頁面中最常見的使用案例。

否則，如果網頁為查看者的容器設定寬度和高度 `DIV`，查看器僅填充該區域並遵循網頁佈局提供的大小。 一個很好的例子是將查看器嵌入到模式覆蓋中，其中覆蓋根據Web瀏覽器窗口大小進行大小調整。

**固定大小嵌入**

通過執行以下操作，可將查看器添加到網頁：

1. 將查看器JavaScript檔案添加到網頁。
1. 定義容器 `DIV`。
1. 設定查看器大小。
1. 建立和初始化查看器。

1. 將查看器JavaScript檔案添加到網頁。

   建立查看器要求在HTML頭中添加指令碼標籤。 在使用查看器API之前，請確保包括 [!DNL Video360Viewer.js]。 的 [!DNL Video360Viewer.js] 檔案位於 [!DNL html5/js/] 標準IS查看器部署的子資料夾：

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js]

如果查看器部署在其中一個Adobe Dynamic Media Classic伺服器上，並且從同一域提供服務，則可以使用相對路徑。 否則，您將指定到安裝了IS-Viewers的Adobe Dynamic Media Classic伺服器之一的完整路徑。

相對路徑如下所示：

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>僅引用主查看器JavaScript `include` 檔案。 不要引用網頁代碼中任何可能在運行時由查看器邏輯下載的附加JavaScript檔案。 特別是，不直接引用HTML5 SDK `Utils.js` 由查看器從 `/s7viewers` 上下文路徑（所謂統一SDK） `include`)。 原因是 `Utils.js` 或類似的運行時查看器庫由查看器的邏輯和查看器版本之間的位置更改進行完全管理。 Adobe不保留舊版次查看器 `includes` 在伺服器上。
>
>
>因此，直接引用任何輔助JavaScript `include` 該頁面上的查看器使用的瀏覽器功能將在部署新產品版本時中斷查看器功能。

1. 定義容器 `DIV`。

   添加空 `DIV` 元素。 的 `DIV` 元素必須定義其ID，因為此ID稍後會傳遞給查看器API。 DIV的大小通過CSS指定。

   佔位符 `DIV` 是定位元素，表示 `position` CSS屬性設定為 `relative` 或 `absolute`。

   要使全屏功能在Internet Explorer中正常工作，請確保DOM中沒有其他元素的堆疊順序高於佔位符 `DIV`。

   以下是定義佔位符的示例 `DIV` 元素：

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div>
   ```

1. 設定查看器大小

   可以通過為聲明查看器來設定其靜態大小 `.s7video360viewer` 頂級CSS類（以絕對單位表示），或使用 `stagesize` 修改量。

   您可以將大小調整直接放在CSS中的HTML頁或自定義查看器CSS檔案中，該檔案稍後將分配給Adobe Experience Manager資產 — 按需分配的查看器預設記錄，或使用顯式傳遞 `style` 的子菜單。

   請參閱 [自定義Video360查看器](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) 的子菜單。

   下面是在HTML頁中定義靜態查看器大小的示例：

   ```html {.line-numbers}
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   可以設定 `stagesize` 在AEM Assets的查看器預設記錄中的修飾符 — 按需。 或者，可以使用查看器初始化代碼顯式傳遞它， `params` 或作為「命令引用」部分中所述的API調用，如下所示：

   ```html {.line-numbers}
   video360viewer.setParam("stagesize", "640,640");
   ```

   建議使用基於CSS的方法，並在本示例中使用。

1. 建立和初始化查看器。

   完成上述步驟後，將建立 `s7viewers.Video360Viewer` 類，將所有配置資訊傳遞給其建構子，並調用 `init()` 的子常式。 配置資訊作為JSON對象傳遞給建構子。 至少，此對象應 `containerId` 包含查看器容器ID名稱和嵌套的欄位 `params` 具有查看器支援的配置參數的JSON對象。

   在這個例子中， `params` 對象必須至少將Image Serving URL傳遞為 `serverUrl` 及初始資產 `asset` 的下界。 通過基於JSON的初始化API，您可以建立並啟動查看器，並使用一行代碼、傳遞為 `videoserverurl` 物業、初始資產 `asset` 參數和交互資料 `interactivedata` 屬性。 基於JSON的初始化API允許您使用單行代碼建立和啟動查看器。

   必須將查看器容器添加到DOM中，以便查看器代碼可以通過其ID查找容器元素。 某些瀏覽器將生成DOM延遲到網頁結束。 要獲得最大相容性，請調用 `init()` 方法 `BODY` 標籤，或者身上 `onload()` 的子菜單。

   同時，容器元素還不一定是網頁佈局的一部分。 例如，它可能隱藏在 `display:none` 指定的樣式。 在這種情況下，查看器將其初始化過程延遲到網頁將容器元素帶回佈局的那一刻。 當這種情況發生時，查看器載入將自動恢復。

   以下是建立查看器實例的示例，將最小必要配置選項傳遞給建構子，並調用 `init()` 的雙曲餘切值。 該示例假定：

   * 查看器實例為 `video360Viewer`。
   * 佔位符的名稱 `DIV` 是 `s7viewer`。
   * 影像服務URL為 `https://s7d9.scene7.com/is/image`。
   * 視頻伺服器URL為 `https://s7d9.scene7.com/is/content`。
   * 資產 `Viewers/space_station_360-AVS`。

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var video360Viewer = new s7viewers.Video360Viewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/space_station_360-AVS", 
    "serverurl":"https://s7d9.scene7.com/is/image/", 
    "videoserverurl":"https://s7d9.scene7.com/is/content/" 
   } 
   }).init(); 
   </script>
   ```

   以下代碼是嵌入Video360 Viewer且大小固定的普通網頁的完整示例：

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   <script type="text/javascript"> 
   var video360Viewer = new s7viewers.Video360Viewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/space_station_360-AVS", 
    "serverurl":"https://s7d9.scene7.com/is/image/", 
    "videoserverurl":"https://s7d9.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**具有無限制高度的響應設計嵌入**

通過響應性設計嵌入，網頁通常具有某種靈活的佈局，其指示查看者容器的運行時大小 `DIV`。 對於以下示例，假定該網頁允許查看者的容器 `DIV` 以取Web瀏覽器窗口大小的40%，使其高度不受限制。 網頁HTML代碼如下所示：

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

將查看器添加到此頁麵類似於固定大小嵌入的步驟。 唯一的區別是您不需要顯式定義查看器大小。

1. 將查看器JavaScript檔案添加到網頁。
1. 定義容器DIV。
1. 建立和初始化查看器。

上述步驟與固定尺寸嵌入步驟相同。 將容器DIV添加到現有 `"holder"` DIV 以下代碼是一個完整的示例。 注意當瀏覽器調整大小時查看器大小如何變化，以及查看器縱橫比如何匹配資產。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
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
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**定義寬度和高度的響應嵌入**

如果定義了寬度和高度的響應嵌入，則網頁樣式是不同的。 它為 `"holder"` DIV並將其置於瀏覽器窗口中。 此外，網頁還設定 `HTML` 和 `BODY` 元素到100%。

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

其餘的嵌入步驟與用於具有無限制高度的響應嵌入的步驟相同。 結果示例如下：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
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
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**使用基於Setter的API嵌入**

可以不使用基於JSON的初始化，而是使用基於setter的API和no-args建構子。 使用此API建構子不採用任何參數，配置參數是使用 `setContainerId()`。 `setParam()`, `setAsset()` API方法，具有單獨的JavaScript調用。

以下示例說明了將固定大小嵌入與基於setter的API一起使用：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7video360viewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var video360Viewer = new s7viewers.Video360Viewer(); 
video360Viewer.setContainerId("s7viewer"); 
video360Viewer.setParam("serverurl", "https://s7d9.scene7.com/is/image/"); 
video360Viewer.setParam("videoserverurl", "https://s7d9.scene7.com/is/content/"); 
video360Viewer.setAsset("Viewers/space_station_360-AVS"); 
video360Viewer.init(); 
</script> 
</body> 
</html>
```
