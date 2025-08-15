---
title: 互動影像
description: 互動式影像檢視器是一種檢視器，可顯示單一不可縮放影像，其中包含可點按的熱點。 此檢視器的目的是實作「可購物橫幅」體驗。 也就是說，使用者可以在橫幅影像上選取熱點，並重新導向至您網站上的快速檢視或產品詳細資料頁面。 專為桌上型電腦和行動裝置所設計。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: c7089ecd-6ff3-4fe9-9ee7-3b48c9201558
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '1703'
ht-degree: 0%

---

# 互動影像{#interactive-image}

互動式影像檢視器是一種檢視器，可顯示單一不可縮放影像，其中包含可點按的熱點。 此檢視器的目的是實作「可購物橫幅」體驗。 也就是說，使用者可以在橫幅影像上選取熱點，並重新導向至您網站上的快速檢視或產品詳細資料頁面。 專為桌上型電腦和行動裝置所設計。

>[!NOTE]
>
>此檢視器不支援使用IR （影像演算）或UGC （使用者產生的內容）的影像。

檢視器型別為508。

## 示範URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage.html)

## 系統要求 {#section-b7270cc4290043399681dc504f043609}

請參閱[系統需求](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

## 使用互動式影像檢視器 {#section-e6c68406ecdc4de781df182bbd8088b4}

互動式影像檢視器代表主要JavaScript檔案和一組協助程式檔案(單一JavaScript包含此特定檢視器使用的所有Viewer SDK元件、資產、CSS)，這些檔案由檢視器在執行階段下載。

互動式影像檢視器僅能用於內嵌模式，也就是使用檔案說明的API整合至目標網頁。

組態和外觀設定類似於本說明中描述的其他檢視器。 所有外觀設定都是透過自訂CSS來達成。

檢視所有檢視器通用的[命令參考 — 組態屬性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)和所有檢視器通用的[命令參考 — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 與互動式影像檢視器互動 {#section-642e66ca38cd4032992840ec6c0b0cd2}

視訊影像檢視器支援的互動是案頭系統上的熱點啟用。 此啟動會在點選和點一下觸控裝置上進行。

檢視器可使用完整的鍵盤。

請參閱[鍵盤協助工具與導覽](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 內嵌互動式影像檢視器 {#section-6bb5d3c502544ad18a58eafe12a13435}

互動式影像檢視器內嵌於託管頁面。 這類網頁可能具有靜態版面，也可能是「回應式」的，且在不同裝置或不同瀏覽器視窗大小中顯示時不同。

為因應這些需求，檢視器支援兩種主要操作模式：固定大小內嵌和回應式內嵌。

**關於固定大小內嵌模式和回應式設計內嵌模式**

在內嵌模式中，檢視器會新增至現有網頁。 此網頁可能已有某些與檢視器無關的客戶內容。 檢視器通常只會佔用網頁的一部分空間。

主要使用案例是針對桌上型電腦或平板電腦裝置的網頁，以及可依據裝置型別自動調整版面的回應式設計頁面。

當檢視器在初始載入後未變更其大小時，會使用固定大小內嵌。 此方法適用於具有靜態配置的網頁。

回應式設計內嵌假設檢視器必須在執行階段調整大小，以回應其容器`DIV`的大小變更。 最常見的使用案例是將檢視器新增到使用彈性頁面配置的網頁。

在回應式設計內嵌模式中，檢視器的行為會因網頁大小其容器`DIV`的方式而異。 如果網頁僅設定容器`DIV`的寬度，而不限制其高度，檢視器會根據所使用資產的外觀比例，自動選擇其高度。 此功能可確保資產完全符合檢視方式，且兩側不會有任何邊框間距。 此使用案例最常用於使用回應式網頁設計配置架構(例如Bootstrap和Foundation)的網頁。

否則，如果網頁同時設定檢視器容器`DIV`的寬度和高度，則檢視器只會填滿該區域。 它也能依照網頁版面提供的大小來設定。 一個好的範例是內嵌檢視器至強制回應覆蓋圖，其中覆蓋圖會根據網頁瀏覽器視窗大小而調整。

**固定大小內嵌**

您可以執行下列動作，將檢視器新增至網頁：

1. 正在將viewer JavaScript檔案新增至您的網頁。
1. 定義容器`DIV`。
1. 設定檢視器大小。
1. 正在建立和初始化檢視器。

1. 正在將viewer JavaScript檔案新增至您的網頁。

   建立檢視器需要您在HTML標題中新增指令碼標籤。 在可以使用檢視器API之前，請確定您已包含[!DNL InterativeImage.js]。 [!DNL InteractiveImage.js]檔案位於標準IS-Viewers部署的[!DNL html5/js/]子資料夾下：

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js]

如果檢視器部署在任一Adobe Dynamic Media Classic伺服器上，且從相同網域提供服務，您就可以使用相對路徑。 否則，請指定已安裝IS-Viewers之其中一個Adobe Dynamic Media Classic伺服器的完整路徑。

相對路徑如下所示：

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script>
```

>[!NOTE]
>
>僅參考頁面上的主要檢視器JavaScript `include`檔案。 請勿在網頁程式碼中參考任何其他JavaScript檔案（這些檔案可能由執行階段的檢視器邏輯下載）。 特別是，請勿直接參考檢視器從`Utils.js`內容路徑(所謂整合的HTML `/s7viewers`)載入的SDK5 SDK `include`資料庫。 原因在於`Utils.js`或類似的執行階段檢視器程式庫的位置完全由檢視器的邏輯管理，且位置會在檢視器發行版本之間變更。 Adobe不會在伺服器上保留舊版的次要檢視器`includes`。
>
>
>因此，日後部署新產品版本時，將檢視器使用的任何次要JavaScript `include`的直接參照放在頁面上，會中斷檢視器功能。

1. 定義容器`DIV`。

   新增空的`DIV`元素至您要檢視器出現的頁面。 `DIV`專案必須定義其ID，因為此ID稍後會傳遞至檢視器API。 DIV的大小是透過CSS指定。

   預留位置`DIV`是定位元素，表示`position` CSS屬性設定為`relative`或`absolute`。

   以下是已定義的預留位置`DIV`元素的範例：

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. 設定檢視器大小

   您可以透過以絕對單位宣告`.s7interactiveimage`頂層CSS類別的檢視器，或使用`stagesize`修飾元來設定檢視器的靜態大小。

   您可以直接在HTML頁面上調整CSS的大小。 或者，您可以將大小調整放入自訂檢視器CSS檔案中，稍後再將該檔案指派給Adobe Experience Manager Assets中的檢視器預設集記錄（隨選），或使用`style`命令明確傳遞。

   請參閱[影片](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0)，以取得使用CSS設定檢視器樣式的詳細資訊。

   以下是在HTML頁面中定義靜態檢視器大小的範例：

   ```html {.line-numbers}
   #s7viewer.s7interactiveimage { 
    width: 1174px; 
    height: 500px; 
   }
   ```

   您可以使用檢視器初始化程式碼和`stagesize`集合明確傳遞`params`修飾元，或如Command Reference一節中所述，以API呼叫形式傳遞，如下所示：

   ```html {.line-numbers}
   interactiveImage.setParam("stagesize", "1174,500");
   ```

   此範例建議您使用以CSS為基礎的方法。

1. 正在建立和初始化檢視器。

   完成上述步驟後，您會建立`s7viewers.InteractiveImage`類別的執行個體、將所有組態資訊傳遞至其建構函式，並在檢視器執行個體上呼叫`init()`方法。 組態資訊會以JSON物件的形式傳遞至建構函式。 此物件至少應有`containerId`欄位，其內含檢視器容器ID的名稱，以及含有檢視器支援之組態引數的巢狀`params` JSON物件。 在此情況下，`params`物件必須至少將影像伺服URL傳遞為`serverUrl`屬性，並將初始資產傳遞為`asset`引數。 JSON型初始化API可讓您使用一行程式碼來建立和啟動檢視器。

   請務必將檢視器容器新增至DOM，讓檢視器程式碼可依其ID尋找容器元素。 有些瀏覽器會延遲建立DOM，直到網頁結尾為止。 為達到最大相容性，請在結尾的`init()`標籤前面或內文`BODY`事件上呼叫`onload()`方法。

   同時，容器元素也不一定屬於網頁版面配置的一部分。 例如，可以使用指派給它的`display:none`樣式來隱藏它。 在此情況下，檢視器會延遲其初始化程式，直到網頁將容器元素帶回版面配置為止。 發生此事件時，檢視器會自動繼續載入。

   以下是建立檢視器執行個體、將最低必要組態選項傳遞至建構函式及呼叫`init()`方法的範例。 此範例假設`interactiveImage`為檢視器執行個體；`s7viewer`為預留位置`DIV`的名稱；`http://aodmarketingna.assetsadobe.com/is/image`為影像伺服URL，`/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.`為資產：

   ```html {.line-numbers}
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

   下列程式碼為將視訊影像檢視器嵌入固定大小的簡單網頁的完整範例：

   ```html {.line-numbers}
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

**高度不受限制的回應式設計內嵌**

透過回應式設計內嵌，網頁通常會有某種彈性的配置，可指定檢視器容器`DIV`的執行階段大小。 對於下列範例，假設網頁允許檢視器的容器`DIV`取得網頁瀏覽器視窗大小的40%。 而且，其高度不受限制。 網頁HTML程式碼如下所示：

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

將檢視器新增至這類頁面，類似於固定大小內嵌的步驟。 唯一的區別是您不需要明確定義檢視器大小。

1. 正在將viewer JavaScript檔案新增至您的網頁。
1. 定義容器`DIV`。
1. 正在建立和初始化檢視器。

上述所有步驟與內嵌固定大小相同。 將容器`DIV`新增至現有的`"holder"` `DIV`。 下列程式碼為完整的範例。 請注意瀏覽器調整大小時檢視器大小的變化，以及檢視器外觀比例與資產的相符情形。

```html {.line-numbers}
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

以下範例頁面說明高度不受限制的回應式設計內嵌在實際應用中的更多情況：

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage-responsive-unrestricted-height.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage-responsive-unrestricted-height.html)

定義寬度和高度的&#x200B;**彈性大小內嵌**

如果有已定義寬度和高度的彈性大小內嵌，則網頁樣式會不同。 它同時提供大小給`"holder"` DIV，並將它置中於瀏覽器視窗中。 此外，網頁會將`HTML`和`BODY`專案的大小設定為100%。

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

其餘的內嵌步驟與高度不受限制的回應式內嵌步驟相同。 產生的範例如下：

```html {.line-numbers}
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

**使用Setter型API內嵌**

除了使用JSON型初始化之外，也可以使用setter型API和no-args建構函式。 使用此API建構函式不會接受任何引數，而設定引數是使用`setContainerId()`、`setParam()`和`setAsset()` API方法搭配個別的JavaScript呼叫所指定。

下列範例說明如何將固定大小內嵌與setter型API搭配使用：

```html {.line-numbers}
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
