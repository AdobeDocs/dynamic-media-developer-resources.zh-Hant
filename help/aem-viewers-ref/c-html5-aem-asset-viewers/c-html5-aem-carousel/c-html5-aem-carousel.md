---
title: 轉盤
description: Carousel Viewer是一個查看器，它顯示帶有可按一下熱點或區域的非可縮放橫幅影像的Carousel。 此查看器可幫助您實現「可購物的旋轉傳送」體驗，用戶可以在橫幅影像上選擇熱點或區域。 他們可以重定向到客戶網站上的Quickview或產品詳細資訊頁面。 它設計用於台式機和移動設備。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: d506dc6e-8929-4f7f-a205-1683e77681f1
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '1888'
ht-degree: 0%

---

# 轉盤{#carousel}

Carousel Viewer是一個查看器，它顯示帶有可按一下熱點或區域的非可縮放橫幅影像的Carousel。 此查看器可幫助您實現「可購物的旋轉傳送」體驗，用戶可以在橫幅影像上選擇熱點或區域。 他們可以重定向到客戶網站上的Quickview或產品詳細資訊頁面。 它設計用於台式機和移動設備。

>[!NOTE]
>
>此查看器不支援使用影像呈現或用戶生成內容(UGC)的影像。

查看器類型為511。

## 演示URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/carousel/CarouselViewerDemo.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/carousel/CarouselViewerDemo.html)

## 系統要求 {#section-b7270cc4290043399681dc504f043609}

請參閱 [系統要求](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

## 使用旋轉軸查看器 {#section-e6c68406ecdc4de781df182bbd8088b4}

Carousel查看器表示主JavaScript檔案和一組幫助程式檔案（單個JavaScript包含該查看器在運行時下載的所有Viewer SDK元件，該查看器由該特定查看器、資產和CSS使用）。

Carousel查看器既可以使用隨IS查看器提供的生產就緒HTML頁在彈出模式下使用，也可以使用使用文檔化API將其整合到目標網頁的嵌入式模式。

配置和外觀與本幫助中描述的其他查看器的配置和外觀相似。 所有蒙皮都是通過自定義CSS實現的。

請參閱 [所有查看器通用的命令引用 — 配置屬性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 和 [所有查看器通用的命令引用 — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 與旋轉木馬查看器交互 {#section-642e66ca38cd4032992840ec6c0b0cd2}

在旋轉軸集中導航是通過在主視圖上水準滑動或在案頭設備上使用兩個箭頭按鈕來完成的。 設定指示器點顯示設定內的當前位置。

查看器可以呈現橫幅影像頂部的熱點或區域，以指示產品上的交互區域。

按一下或點擊某個熱點或某個區域會在創作期間觸發與其關聯的操作。 該動作可以被重定向到網站上的不同頁面，或者它可以將產品資訊傳回網頁邏輯，而網頁邏輯又可以觸發具有相關產品內容的Quickview。

可以完全使用鍵盤訪問查看器。

請參閱 [鍵盤輔助功能和導航](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 嵌入旋轉軸查看器 {#section-6bb5d3c502544ad18a58eafe12a13435}

**關於彈出模式**

在彈出模式下，在單獨的Web瀏覽器窗口或頁籤中開啟查看器。 它會佔用整個瀏覽器窗口區域，並在瀏覽器調整大小或移動設備的方向發生變化時進行調整。

彈出模式是移動設備中最常見的模式。 網頁使用 `window.open()` JavaScript調用，正確配置 `A` HTML元件或任何其它合適的方法。

建議您使用現成HTML頁面進行彈出操作模式。 在這種情況下，它叫 `CarouselViewer.html` 位於 `html5/` 標準IS查看器部署的子資料夾：

`<s7viewers_root>/html5/CarouselViewer.html`

通過應用自定義CSS，可以實現可視化定製。

以下是在新窗口中開啟查看器的HTML代碼示例：

```html {.line-numbers}
<a href="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/CarouselViewer.html?asset=/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner&serverurl=https://adobedemo62-h.assetsadobe.com/is/image" target="_blank">Open popup viewer</a>
```

**關於固定尺寸嵌入模式和響應設計嵌入模式**

在嵌入模式中，查看器被添加到現有網頁。 此網頁可能已包含一些與查看器無關的客戶內容。 瀏覽者通常只佔用網頁的一部分房地產。

主要使用案例是面向台式機或平板電腦設備的網頁，以及響應性設計的頁面，這些頁面根據設備類型自動調整佈局。

當查看器在初始載入後不更改其大小時，使用固定大小嵌入。 此方法是具有靜態佈局的網頁的最佳選擇。

響應性設計嵌入假定查看器必須在運行時根據其容器的大小變化調整大小 `DIV`。 最常見的用例是向使用靈活頁面佈局的網頁添加查看器。

在響應性設計嵌入模式中，查看器根據網頁大小其容器的方式而具有不同的行為 `DIV`。 如果網頁僅設定容器的寬度 `DIV`在保持高度不受限制的情況下，觀看者根據所使用資產的縱橫比自動選擇其高度。 此功能可確保資產完美地貼入視圖中，而不會在側面出現任何填充。 此使用案例是使用響應性Web設計佈局框架(如Bootstrap和Foundation)的Web頁面中最常見的使用案例。

否則，如果網頁為查看者的容器設定寬度和高度 `DIV`，查看器將填充該區域。 它還遵循網頁佈局提供的大小。 一個很好的例子是將查看器嵌入到模式覆蓋中，其中覆蓋根據Web瀏覽器窗口大小進行大小調整。

**固定大小嵌入**

通過執行以下操作，可將查看器添加到網頁：

1. 將查看器JavaScript檔案添加到網頁。
1. 定義容器 `DIV`。
1. 設定查看器大小。
1. 建立和初始化查看器。

1. 將查看器JavaScript檔案添加到網頁。

   建立查看器要求在HTML頭中添加指令碼標籤。 在使用查看器API之前，請確保包括 [!DNL CarouselViewer.js]。 的 [!DNL CarouselViewer.js] 檔案位於 [!DNL html5/js/] 標準IS查看器部署的子資料夾：

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js]

如果查看器部署在其中一個Adobe Dynamic Media Classic伺服器上，並且從同一域提供服務，則可以使用相對路徑。 否則，您將指定到安裝了IS-Viewers的Adobe Dynamic Media Classic伺服器之一的完整路徑。

相對路徑如下所示：

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script>
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

   以下是定義佔位符的示例 `DIV` 元素：

   ```CSS {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. 設定查看器大小

   可以通過為聲明查看器來設定其靜態大小 `.s7carouselviewer` 頂級CSS類（以絕對單位表示），或使用 `stagesize` 修改量。

   您可以將大小調整直接放在CSS中的HTML頁。 或者，您可以將大小調整放在自定義查看器CSS檔案中，該檔案稍後會分配給AEM Assets的查看器預設記錄 — 按需分配，或使用 `style` 的子菜單。

   請參閱 [自定義旋轉軸查看器](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/c-html5-aem-carousel-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) 的子菜單。

   下面是在HTML頁中定義靜態查看器大小的示例：

   ```CSS {.line-numbers}
   #s7viewer.s7carouselviewer { 
    width: 1174px; 
    height: 500px; 
   }
   ```

   您可以顯式 `stagesize` 具有查看器初始化代碼的修改符 `params` 或作為API調用（如「命令參考」部分中所述），如下所示：

   ```CSS {.line-numbers}
   carouselViewer.setParam("stagesize", "1174,500");
   ```

   建議使用基於CSS的方法，並在本示例中使用。

1. 建立和初始化查看器。

   完成上述步驟後，將建立 `s7viewers.CarouselViewer` 類，將所有配置資訊傳遞給其建構子，並調用 `init()` 的子常式。 配置資訊作為JSON對象傳遞給建構子。 至少，此對象應 `containerId` 包含查看器容器ID和嵌套名稱的欄位 `params` 具有查看器支援的配置參數的JSON對象。 在這個例子中， `params` 對象必須至少將Image Serving URL傳遞為 `serverUrl` 及初始資產 `asset` 的下界。 基於JSON的初始化API允許您使用單行代碼建立和啟動查看器。

   必須將查看器容器添加到DOM中，以便查看器代碼可以通過其ID查找容器元素。 某些瀏覽器將生成DOM延遲到網頁結束。 要獲得最大相容性，請調用 `init()` 方法 `BODY` 標籤，或者身上 `onload()` 的子菜單。

   同時，容器元素還不一定是網頁佈局的一部分。 例如，它可能隱藏在 `display:none` 指定的樣式。 在這種情況下，查看器將其初始化過程延遲到網頁將容器元素帶回佈局的那一刻。 當此功能出現時，查看器載入將自動恢復。

   以下是建立查看器實例、將最小必要配置選項傳遞給建構子並調用 `init()` 的雙曲餘切值。 該示例假定 `carouselViewer` 是查看器實例； `s7viewer` 是佔位符的名稱 `DIV`; `https://adobedemo62-h.assetsadobe.com/is/image` 是影像服務URL, `/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner` 是資產：

   ```javascript {.line-numbers}
   <script type="text/javascript"> 
   var carouselViewer = new s7viewers.CarouselViewer ({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
    "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script>
   ```

   以下代碼是嵌入固定大小的Carousel查看器的普通網頁的完整示例：

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7carouselviewer { 
    width: 1174px; 
    height: 500px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var carouselViewer = new s7viewers.CarouselViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
    "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**具有無限制高度的響應設計嵌入**

通過響應性設計嵌入，網頁通常具有某種靈活的佈局，其指示查看者容器的運行時大小 `DIV`。 對於以下示例，假定該網頁允許查看者的容器 `DIV` 以獲取40%的Web瀏覽器窗口大小。 而且它的高度沒有限制。 網頁HTML代碼如下所示：

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

將查看器添加到此頁麵類似於固定大小嵌入的步驟。 唯一的區別是您不需要顯式定義查看器大小。

1. 將查看器JavaScript檔案添加到網頁。
1. 定義容器 `DIV`。
1. 建立和初始化查看器。

上述步驟與固定尺寸嵌入步驟相同。 添加容器 `DIV` 到現有 `"holder"` `DIV`。 以下代碼是一個完整的示例。 注意在調整瀏覽器大小時查看器大小如何變化，以及查看器縱橫比如何與資產匹配。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
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
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html>
```

以下示例頁說明了具有無限制高度的響應設計嵌入在現實生活中的更多用途：

[https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/carousel/CarouselViewer-responsive-unrestricted-height.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/carousel/CarouselViewer-responsive-unrestricted-height.html)

**定義寬高的柔性尺寸嵌入**

在定義了寬度和高度的柔性大小嵌入中，網頁樣式是不同的。 它為 `"holder"` DIV並將其置於瀏覽器窗口中。 此外，網頁還設定 `HTML` 和 `BODY` 元素到100%。

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
<script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
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
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
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
<script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7carouselviewer { 
 width: 1174px; 
 height: 500px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var carouselViewer = new s7viewers.CarouselViewer(); 
carouselViewer.setContainerId("s7viewer"); 
carouselViewer.setParam("serverurl", "https://adobedemo62-h.assetsadobe.com/is/image"); 
carouselViewer.setAsset("/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner"); 
carouselViewer.init(); 
</script> 
</body> 
</html>
```
