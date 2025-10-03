---
title: 混合媒體
description: 混合媒體檢視器是一種媒體檢視器。 它支援包含影像、色票集、迴轉集、視訊和自我調整視訊集的媒體集。
keywords: 回應式
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 65a54308-f9db-4458-a9c3-ccb1433af43c
source-git-commit: 4964c2ac68b4baab7347d6d0e26e2237995720e8
workflow-type: tm+mt
source-wordcount: '2511'
ht-degree: 0%

---

# 混合媒體{#mixed-media}

混合媒體檢視器是一種媒體檢視器。 它支援包含影像、色票集、迴轉集、視訊和自我調整視訊集的媒體集。

檢視器底部的縮圖代表每個媒體集元素，及其資產型別指標。 選取色票集元素時，會出現第二列的色票，以允許選取色票集內的顏色變化。 影像和色票集元素支援以連續或內嵌模式縮放；迴轉集支援縮放和旋轉。 視訊和自我調整視訊集支援所有基本播放控制項，只要視訊內容上方顯示任何選用的隱藏式字幕即可。 使用者可隨時按一下全熒幕按鈕以切換至全熒幕。 檢視器有選用的關閉按鈕。 專為桌上型電腦和行動裝置所設計。

只要基礎系統支援，混合媒體檢視器就會在其預設設定中，使用HLS格式的HTML5串流視訊播放。 在不支援HTML5串流的系統上，檢視器會回到HTML5漸進式視訊傳送。

>[!NOTE]
>
>此檢視器不支援使用IR （影像演算）或UGC （使用者產生的內容）的影像。

檢視器型別505。

請參閱[系統需求和先決條件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

## 示範URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

## 使用混合媒體檢視器 {#section-f21ac23d3f6449ad9765588d69584772}

混合媒體檢視器代表主要JavaScript檔案和一組協助程式檔案(單一JavaScript包含此特定檢視器使用的所有Viewer SDK元件、資產、CSS)，這些檔案由檢視器在執行階段下載。

您可以使用隨附於IS-Viewers的生產就緒HTML頁面，在快顯視窗模式中使用混合媒體檢視器。 或者，您可以在內嵌模式中使用檢視器，其中使用檔案化的API將其整合至目標網頁。

設定檢視器外觀的工作與其他檢視器類似。 所有外觀設定都是透過自訂CSS來達成。

檢視所有檢視器通用的[命令參考 — 組態屬性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)和所有檢視器通用的[命令參考 — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 與混合媒體檢視器互動 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

混合媒體檢視器支援其他行動應用程式中常見的單一觸控和多重觸控手勢。 當檢視器無法處理使用者的撥動手勢時，會轉送事件給網頁瀏覽器以執行原生頁面捲動。 即使檢視器佔據裝置熒幕區域的大部分，此功能仍可讓使用者導覽頁面。

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>手勢 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>點一下滑鼠 </p> </td> 
   <td colname="col2"> <p> 啟動彈出式檢視或在主要和次要縮放層級之間變更。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>點兩下 </p> </td> 
   <td colname="col2"> <p>在<span class="codeph">連續</span>縮放模式中，放大一個層級，直到達到最大放大率，下一個雙點手勢會重設為初始狀態。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>觸摸並停留 </p> </td> 
   <td colname="col2"> <p> 在<span class="codeph">內嵌</span>縮放模式中時，會啟用縮放的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>捏合 </p> </td> 
   <td colname="col2"> <p>在連續縮放模式中，放大或縮小影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>水準撥動或輕觸 </p> </td> 
   <td colname="col2"> <p> 當目前資產為迴轉集且影像處於重設狀態時，會水準迴轉該迴轉集。 </p> <p> 當目前資產為迴轉集或影像，且影像已放大時，會水準移動影像。 如果影像移至檢視邊緣，而且仍在該方向完成撥動，手勢會執行原生頁面捲動。 </p> <p> 在色票列中捲動色票清單。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直撥動或輕觸 </p> </td> 
   <td colname="col2"> <p> 如果影像處於重設狀態，則會在使用多維度迴轉集時變更垂直檢視角度。 在一維迴轉集內，或多維迴轉集位於最後一個或第一個軸上，使得垂直撥動不會導致垂直檢視角度變更時，手勢會執行原生頁面捲動。 </p> <p> 當目前資產為迴轉集或影像，且影像已放大時，會垂直移動影像。 如果影像移至檢視邊緣後仍沿該方向滑動，手勢會執行原生頁面捲動。 </p> <p> 如果該手勢是在色票區域內完成，則會執行原生頁面捲動。 </p> </td> 
  </tr> 
 </tbody> 
</table>

該檢視器也支援在具備觸控熒幕和滑鼠的Windows裝置上進行觸控輸入和滑鼠輸入。 不過，這項支援僅限Chrome、Internet Explorer 11和Edge網頁瀏覽器。

此檢視器可使用完整的鍵盤。

請參閱[鍵盤協助工具與導覽](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 內嵌混合媒體檢視器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同的網頁對檢視者的行為有不同的需求。 有時，網頁會提供連結，在選取時會在個別瀏覽器視窗中開啟檢視器。 在其他情況下，需要直接將檢視器內嵌在託管頁面中。 在後一種情況下，網頁可能會有靜態頁面佈局，或使用在不同裝置上或不同瀏覽器視窗大小下顯示不同的回應式設計。 為了滿足這些需求，檢視器支援三種主要操作模式：快顯視窗、固定大小嵌入和回應式設計嵌入。

## 關於彈出式模式 {#section-77d5aa03b8b94566958a179b1a2cd474}

在快顯視窗模式中，檢視器會在個別的網頁瀏覽器視窗或標籤中開啟。 它會取用整個瀏覽器視窗區域，並在瀏覽器調整大小或行動裝置方向變更時進行調整。

快顯視窗模式最常用於行動裝置。 網頁會使用`window.open()` JavaScript呼叫、正確設定的`A` HTML元素或任何其他適當的方法載入檢視器。

建議您為快顯視窗操作模式使用現成可用的HTML頁面。 在此案例中，其名稱為[!DNL MixedMediaViewer.html]，且位於標準IS-Viewers部署的[!DNL html5/]子資料夾內：

[!DNL <s7viewers_root>/html5/MixedMediaViewer.html]

您可以套用自訂CSS以實現視覺化自訂。

以下是在新視窗中開啟檢視器的HTML程式碼範例：

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample" target="_blank">Open popup viewer</a>
```

## 關於固定大小和回應式設計內嵌 {#section-ec86b100ba5943d0b16694268520bbde}

在內嵌模式中，檢視器會新增至現有網頁，其中可能已有某些與檢視器無關的客戶內容。 檢視器通常只會佔用網頁的一部分空間。

主要使用案例是桌上型電腦或平板電腦裝置導向的網頁，以及可依據裝置型別自動調整版面的回應式設計頁面。

當檢視器在初始載入後未變更其大小時，會使用固定大小內嵌。 此動作是含有靜態佈局的網頁的最佳選擇。

回應式設計內嵌假設檢視器必須在執行階段調整大小，以回應其容器`DIV`的大小變更。 最常見的使用案例是將檢視器新增到使用彈性頁面配置的網頁。

在回應式設計內嵌模式中，檢視器的行為會因網頁大小其容器`DIV`的方式而異。 如果網頁僅設定容器`DIV`的寬度，而不限制其高度，檢視器會根據所使用資產的外觀比例，自動選擇其高度。 此功能可確保資產完全符合檢視方式，且兩側不會有任何邊框間距。 此使用案例最常用於使用回應式設計配置架構(例如Bootstrap或Foundation)的網頁。

否則，如果網頁同時設定檢視器容器`DIV`的寬度和高度，則檢視器只會填滿該區域，並遵循網頁配置所提供的大小。 一個好的範例是內嵌檢視器至強制回應覆蓋圖，其中覆蓋圖會根據網頁瀏覽器視窗大小而調整。

## 固定大小內嵌 {#section-17d162f76ffa4804b27928f51e7bea1d}

您可以執行下列動作，將檢視器新增至網頁：

1. 正在將viewer JavaScript檔案新增至您的網頁。
1. 定義容器`DIV`。
1. 設定檢視器大小。
1. 正在建立和初始化檢視器。

1. 正在將viewer JavaScript檔案新增至您的網頁。

   建立檢視器需要您在HTML標題中新增指令碼標籤。 在可以使用檢視器API之前，請確定您已包含[!DNL MixedMediaViewer.js]。 [!DNL MixedMediaViewer.js]檔案位於標準IS-Viewers部署的[!DNL html5/js/]子資料夾下：

[!DNL <s7viewers_root>/html5/js/MixedMediaViewer.js]

如果檢視器部署在任一Adobe Dynamic Media Classic伺服器上，且從相同網域提供服務，您就可以使用相對路徑。 否則，請指定已安裝IS-Viewers之其中一個Adobe Dynamic Media Classic伺服器的完整路徑。

相對路徑如下所示：

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/MixedMediaViewer.js"></script>
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

   請確定Internet Explorer中的全熒幕功能可正常運作。 確認DOM中沒有其他元素的棧疊順序高於預留位置DIV。

   以下為已定義預留位置DIV元素的範例：

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. 設定檢視器大小

   此檢視器在處理多專案集時會顯示縮圖。 在桌上型電腦系統上，縮圖會放置在主要檢視的下方。 同時，檢視器允許在執行階段使用`setAsset()` API交換主要資產。 身為開發人員，只要新資產只有一個專案，您就能控制檢視器管理底部縮圖區域的方式。 可以保持外部檢視器大小不變，並讓主檢視增加其高度並佔據縮圖區域。 或者，您可以讓主要檢視大小保持靜態，並摺疊外部檢視器區域，讓網頁內容向上移動。 接著，使用縮圖所留下的自由頁面空間。

   若要保持外部檢視器界限不變，請以絕對單位定義`.s7mixedmediaviewer`最上層CSS類別的大小。 CSS的大小調整可直接放在HTML頁面或自訂檢視器CSS檔案中，並於稍後指派給Dynamic Media Classic中的檢視器預設集記錄，或使用style命令明確傳遞。

   請參閱[自訂混合媒體檢視器](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#concept-61b3410f187c4bf3af09ec813c649bf4)，以取得使用CSS設定檢視器樣式的詳細資訊。

   以下是在HTML頁面中定義靜態外部檢視器大小的範例：

   ```html {.line-numbers}
   #s7viewer.s7mixedmediaviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

<!-- You can see the behavior with a fixed outer viewer area on the following sample page. Notice that when you switch between sets, the outer viewer size does not change:-->

<!--

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-outer-area.html)

-->


若要將主要檢視維度設為靜態，請使用`Container` CSS選取器或使用`.s7mixedmediaviewer .s7container`修飾元，以絕對單位定義內部`stagesize` SDK元件的檢視器大小。

以下範例說明如何為內部`Container` SDK元件定義檢視器大小，以便在切換資產時，主要檢視區域不會變更其大小：

```html {.line-numbers}
#s7viewer.s7mixedmediaviewer .s7container { 
 width: 640px; 
 height: 480px; 
}
```

<!-- The following sample page shows viewer behavior with a fixed main view size. Notice that when you switch between sets, the main view remains static and the web page content moves vertically: -->

<!--

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-main-view.html)

   -->

您可以在Dynamic Media Classic的檢視器預設集記錄中設定`stagesize`修飾元，或透過`params`集合的檢視器初始化程式碼明確傳遞。 或者，如本說明的命令參考一節中所述，作為API呼叫，如下所示：

```html {.line-numbers}
mixedMediaViewer.setParam("stagesize", "640,480");
```

此範例建議您使用以CSS為基礎的方法。

1. 正在建立和初始化檢視器。

   完成上述步驟後，您會建立`s7viewers.MixedMediaViewer`類別的執行個體、將所有組態資訊傳遞至其建構函式，並在檢視器執行個體上呼叫`init()`方法。 組態資訊會以JSON物件的形式傳遞至建構函式。 此物件至少應有`containerId`欄位，其中儲存檢視器容器ID的名稱，以及巢狀`params` JSON物件，其中包含檢視器支援的設定引數。 在此案例中，`params`物件必須至少將影像伺服URL傳遞為`serverUrl`屬性，將視訊伺服器URL傳遞為`videoserverurl`屬性，並將初始資產傳遞為`asset`引數。 JSON型初始化API可讓您使用一行程式碼來建立和啟動檢視器。

   請務必將檢視器容器新增至DOM，讓檢視器程式碼可依其ID尋找容器元素。 有些瀏覽器會延遲建立DOM，直到網頁結尾為止。 為達到最大相容性，請在結尾的`init()`標籤前面或內文`BODY`事件上呼叫`onload()`方法。

   同時，容器元素也不一定屬於網頁版面配置的一部分。 例如，可以使用指派給它的`display:none`樣式來隱藏它。 在此情況下，檢視器會延遲其初始化程式，直到網頁將容器元素帶回版面配置為止。 當此動作發生時，檢視器載入會自動繼續。

   以下是建立檢視器執行個體、將最低必要組態選項傳遞給建構函式，以及呼叫`init()`方法的範例。 此範例假設`mixedMediaViewer`是檢視器執行個體；`s7viewer`是預留位置的名稱`DIV`；[!DNL http://s7d1.scene7.com/is/image/]是影像伺服URL；[!DNL http://s7d1.scene7.com/is/content/]是視訊伺服器URL；[!DNL Scene7SharedAssets/Mixed_Media_Set_Sample]是資產：

```html {.line-numbers}
<script type="text/javascript"> 
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
<script type="text/javascript"> 
mixedMediaViewer.init(); 
</script>
```

下列程式碼是嵌入固定大小混合媒體檢視器的簡單網頁的完整範例：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7mixedmediaviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## 高度不受限制的回應式內嵌 {#section-056cb574713c4d07be6d07cf3c598839}

透過回應式設計內嵌，網頁通常會有某種彈性的配置，可指定檢視器容器`DIV`的執行階段大小。 對於下列範例，假設網頁允許檢視器的容器`DIV`取得網頁瀏覽器視窗大小的40%，其高度不受限制。 網頁HTML程式碼如下所示：

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
1. 定義容器DIV。
1. 正在建立和初始化檢視器。

上述所有步驟與內嵌固定大小相同。 將容器DIV新增至現有的`"holder"` DIV。 下列程式碼為完整的範例。 請注意瀏覽器調整大小時檢視器大小的變化，以及檢視器外觀比例與資產的相符情形。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
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
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

以下範例頁面說明高度不受限制的回應式設計內嵌在實際應用中的更多情況：

[即時示範](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!--

[Alternate demo location](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

-->

## 定義寬度和高度的彈性大小內嵌 {#section-0a329016f9414d199039776645c693de}

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

其餘的嵌入步驟與用於高度不受限制的回應式設計嵌入的步驟相同。 產生的範例如下：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
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
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## 使用Setter型API進行內嵌 {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

除了使用JSON型初始化之外，也可以使用setter型API和no-args建構函式。 使用此API建構函式不會接受任何引數，而設定引數是使用`setContainerId()`、`setParam()`和`setAsset()` API方法，以及個別的JavaScript呼叫所指定。

下列範例說明如何將固定大小內嵌與setter型API搭配使用：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7mixedmediaviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var mixedMediaViewer = new s7viewers.MixedMediaViewer(); 
mixedMediaViewer.setContainerId("s7viewer"); 
mixedMediaViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
mixedMediaViewer.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample"); 
mixedMediaViewer.init(); 
</script> 
</body> 
</html>
```
