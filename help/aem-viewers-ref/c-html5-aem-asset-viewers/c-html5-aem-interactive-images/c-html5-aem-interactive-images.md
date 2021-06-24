---
description: 互動式影像檢視器是一種檢視器，可顯示具有可點按熱點的單一不可縮放影像。 此檢視器的用途是實作「可購買橫幅」體驗。 也就是說，使用者可以在橫幅影像上選取熱點，然後重新導向至您網站上的快速檢視或產品詳細資料頁面。 專為在桌上型電腦和行動裝置上運作而設計。
solution: Experience Manager
title: 互動式影像
feature: Dynamic Media Classic，檢視器， SDK/API，互動式影像
role: Developer,Business Practitioner
exl-id: c7089ecd-6ff3-4fe9-9ee7-3b48c9201558
source-git-commit: e6ff4ed80b22e10fc2bd3fac0f4e39bbf5148f8e
workflow-type: tm+mt
source-wordcount: '1733'
ht-degree: 0%

---

# 互動式影像{#interactive-image}

互動式影像檢視器是一種檢視器，可顯示具有可點按熱點的單一不可縮放影像。 此檢視器的用途是實作「可購買橫幅」體驗。 也就是說，使用者可以在橫幅影像上選取熱點，然後重新導向至您網站上的快速檢視或產品詳細資料頁面。 專為在桌上型電腦和行動裝置上運作而設計。

>[!NOTE]
>
>此檢視器不支援使用IR（影像轉譯）或UGC（使用者產生的內容）的影像。

檢視器類型為508。

## 示範URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage.html)

## 系統要求 {#section-b7270cc4290043399681dc504f043609}

請參閱[系統要求](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

## 使用互動式影像檢視器 {#section-e6c68406ecdc4de781df182bbd8088b4}

互動式影像檢視器代表主要JavaScript檔案和一組協助檔案（單一JavaScript包含此特定檢視器、資產、CSS所使用的所有檢視器SDK元件），由檢視器在執行階段下載。

互動式影像檢視器僅能以內嵌模式使用，並透過記錄的API整合至目標網頁。

設定和外觀與本說明中所述其他檢視器的設定和外觀類似。 所有外觀設定都是透過自訂CSS來達成。

請參閱所有檢視器通用的[命令參考 — 設定屬性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)和所有檢視器通用的[命令參考 — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 與互動式影像檢視器互動 {#section-642e66ca38cd4032992840ec6c0b0cd2}

視頻影像查看器支援的交互是案頭系統上的熱點激活。 只要點選一下，就會在點按和觸控裝置上進行此啟動。

檢視器可完全鍵盤存取。

請參閱[鍵盤輔助功能和導航](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 內嵌互動式影像檢視器 {#section-6bb5d3c502544ad18a58eafe12a13435}

互動式影像檢視器設計為內嵌至托管頁面。 這樣的網頁可以具有靜態版面，或者它可以「響應」，並且在不同設備上或針對不同的瀏覽器窗口大小顯示不同。

為了滿足這些需求，檢視器支援兩種主要操作模式：固定大小內嵌和回應式內嵌。

**關於固定大小嵌入模式和響應式設計嵌入模式**

在內嵌模式中，檢視器會新增至現有網頁。 此網頁可能已有一些與檢視器無關的客戶內容。 觀看者通常只佔有網頁的一部分房地產。

主要使用案例為以桌上型電腦或平板電腦裝置為導向的網頁，以及回應式設計的頁面，這些頁面會根據裝置類型自動調整版面。

當檢視器在初始載入後未變更大小時，會使用固定大小內嵌。 這是靜態版面的網頁最佳選擇。

回應式設計內嵌假設檢視器可能需要在執行階段調整大小，以回應其容器`DIV`的大小變更。 最常見的使用案例是在使用彈性頁面版面的網頁中新增檢視器。

在回應式設計內嵌模式中，檢視器的運作方式會因網頁大小其容器`DIV`而有所不同。 如果網頁僅設定容器的寬度`DIV`，保持高度不受限制，則檢視器會根據所使用資產的外觀比例自動選擇其高度。 此功能可確保資產完全符合檢視，而無需邊框上的邊框間距。 此使用案例是使用回應式網頁設計配置架構(例如Bootstrap、Foundation等)的網頁中最常見的使用案例。

否則，如果網頁同時設定了查看器容器`DIV`的寬度和高度，則查看器只會填充該區域。 它也會遵循網頁版面提供的大小。 一個很好的範例是將檢視器嵌入強制回應覆蓋中，其中覆蓋會根據網頁瀏覽器視窗大小來調整大小。

**固定大小嵌入**

您可以執行下列操作，將檢視器新增至網頁：

1. 將檢視器JavaScript檔案新增至您的網頁。
1. 定義容器`DIV`。
1. 設定檢視器大小。
1. 建立和初始化檢視器。

1. 將檢視器JavaScript檔案新增至您的網頁。

   建立檢視器需要在HTML標題中新增指令碼標籤。 使用檢視器API之前，請務必加入[!DNL InterativeImage.js]。 [!DNL InteractiveImage.js]檔案位於標準IS-Viewers部署的[!DNL html5/js/]子資料夾下：

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js]

如果檢視器部署在其中一個AdobeDynamic Media Classic伺服器上，且是從相同網域提供，則可使用相對路徑。 否則，您需指定安裝IS-Viewers之其中一個AdobeDynamic Media Classic伺服器的完整路徑。

相對路徑如下所示：

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script>
```

>[!NOTE]
>
>您只應在頁面上參考主要檢視器JavaScript `include`檔案。 您不應在網頁程式碼中參考任何其他JavaScript檔案，而檢視器邏輯可能會在執行階段下載這些檔案。 尤其是，請勿直接參考檢視器從`/s7viewers`內容路徑（稱為統一SDK `include`）載入的HTML5 SDK `Utils.js`程式庫。 原因在於，`Utils.js`或類似的執行階段檢視器程式庫的位置，是由檢視器的邏輯完全管理，且檢視器版本之間的位置變更。 Adobe不會在伺服器上保留舊版次要檢視器`includes`。
>
>
>因此，將檢視器使用的任何次要JavaScript `include`的直接參考放在頁面上，會在未來部署新產品版本時中斷檢視器的功能。

1. 定義容器`DIV`。

   將空白的`DIV`元素新增至您希望檢視器顯示的頁面。 `DIV`元素必須已定義其ID，因為此ID稍後會傳遞至檢視器API。 DIV的大小是透過CSS指定。

   佔位符`DIV`是定位的元素，這意味著`position` CSS屬性設定為`relative`或`absolute`。

   以下是定義的佔位符`DIV`元素的示例：

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. 設定檢視器大小

   您可以為檢視器設定靜態大小，方法是以絕對單位為`.s7interactiveimage`頂層CSS類別聲明，或使用`stagesize`修飾詞。

   您可以直接將CSS中的大小調整放在HTML頁面上，或放在自訂檢視器CSS檔案中，該檔案稍後會指派給AEM Assets — 隨選的檢視器預設集記錄，或使用`style`命令明確傳遞。

   如需使用CSS來設定檢視器樣式的詳細資訊，請參閱[Video](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0)。

   以下是在HTML頁面中定義靜態檢視器大小的範例：

   ```
   #s7viewer.s7interactiveimage { 
    width: 1174px; 
    height: 500px; 
   }
   ```

   您可以使用包含`params`集合的檢視器初始化程式碼，或如「命令參考」區段所述，以API呼叫的形式明確傳遞`stagesize`修飾元，如下所示：

   ```
   interactiveImage.setParam("stagesize", "1174,500");
   ```

   建議使用CSS型方法，此範例中會使用。

1. 建立和初始化檢視器。

   完成上述步驟後，可以建立一個`s7viewers.InteractiveImage`類的實例，將所有配置資訊傳遞到其建構子，並在查看器實例上調用`init()`方法。 設定資訊會以JSON物件的形式傳遞至建構函式。 此物件至少應有`containerId`欄位，該欄位包含檢視器容器ID的名稱，並巢狀`params` JSON物件，以及檢視器支援的設定參數。 在此情況下，`params`物件至少必須以`serverUrl`屬性傳遞影像伺服URL，並以`asset`參數傳遞初始資產。 JSON型初始化API可讓您使用一行程式碼來建立和啟動檢視器。

   請務必將檢視器容器新增至DOM，讓檢視器程式碼可以透過其ID來尋找容器元素。 有些瀏覽器會延遲建立DOM，直到網頁結尾為止。 如需最大相容性，請在結尾的`BODY`標籤前，或在內文`onload()`事件上呼叫`init()`方法。

   同時，容器元素還不一定是網頁版面的一部分。 例如，可使用指派給它的`display:none`樣式來隱藏它。 在此情況下，檢視器會延遲其初始化程式，直到網頁將容器元素帶回版面的那一刻為止。 發生此情況時，檢視器載入會自動繼續。

   以下是建立查看器實例、將最小必要配置選項傳遞給建構子並調用`init()`方法的示例。 此範例假設`interactiveImage`為檢視器例項；`s7viewer`是佔位符`DIV`的名稱；`http://aodmarketingna.assetsadobe.com/is/image`是影像伺服URL，而`/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.`是資產：

   ```
   <script type="text/javascript"> 
   var interactiveImage = new s7viewers.InteractiveImage ({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
    "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script> 
   ```

   以下程式碼是內嵌固定大小視訊影像檢視器的簡單網頁的完整範例：

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7interactiveimage { 
    width: 1174px; 
    height: 500px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var interactiveImage = new s7viewers.InteractiveImage({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
    "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html> 
   ```

**無限制高度的回應式設計內嵌**

透過回應式設計內嵌，網頁通常會有某種彈性的版面配置，指定檢視器容器`DIV`的執行階段大小。 在下列範例中，假設網頁允許檢視器的容器`DIV`取用40%的網頁瀏覽器視窗大小。 而且，它的高度不受限制。 網頁HTML程式碼如下所示：

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
1. 定義容器`DIV`。
1. 建立和初始化檢視器。

上述所有步驟與固定大小嵌入相同。 將容器`DIV`新增至現有的`"holder"` `DIV`。 下列程式碼為完整的範例。 注意當瀏覽器調整大小時，檢視器大小會如何變更，以及檢視器外觀比例與資產如何相符。

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
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
var interactiveImage = new s7viewers.InteractiveImage({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
 "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

下列範例頁面說明在實際使用中，不受限制高度的回應式設計內嵌：

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage-responsive-unrestricted-height.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage-responsive-unrestricted-height.html)

**定義寬度和高度的靈活大小嵌入**

若是定義寬度和高度的彈性內嵌，網頁樣式會有所不同。 它會為`"holder"` DIV提供兩種大小，並在瀏覽器視窗中將其置中。 此外，網頁還將`HTML`和`BODY`元素的大小設定為100%。

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
<script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
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
var interactiveImage = new s7viewers.InteractiveImage({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
 "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

**使用基於Setter的API嵌入**

您可以使用setter型API和無目標建構函式，而不使用JSON型初始化。 使用此API建構函式時不會採用任何參數，且會使用具有個別JavaScript呼叫的`setContainerId()`、`setParam()`及`setAsset()` API方法指定設定參數。

以下範例說明如何使用固定大小內嵌搭配setter型API:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
<style type="text/css"> 
#s7viewer.s7interactiveimage { 
 width: 1174px; 
 height: 500px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var interactiveImage = new s7viewers.InteractiveImage(); 
interactiveImage.setContainerId("s7viewer"); 
interactiveImage.setParam("serverurl", "http://aodmarketingna.assetsadobe.com/is/image"); 
interactiveImage.setAsset("/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg"); 
interactiveImage.init(); 
</script> 
</body> 
</html> 
```
