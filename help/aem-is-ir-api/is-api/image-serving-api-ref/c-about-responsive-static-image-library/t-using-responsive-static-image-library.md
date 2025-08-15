---
title: 使用Responsive影像資料庫
description: 若要將Responsive影像庫新增至網頁，並使用庫管理現有影像，請完成下列步驟。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2542b9f3-c398-4dbf-afa3-1671fc4fe72a
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 0%

---

# 使用Responsive影像資料庫{#using-responsive-image-library}

若要將Responsive影像庫新增至網頁，並使用庫管理現有影像，請完成下列步驟。

**使用回應式影像庫**

1. 在Dynamic Media Classic中，[建立影像預設集](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/image-sizing/setting-image-presets.html?lang=zh-Hant#image-sizing)，以備您打算搭配預設集使用回應式影像資料庫時使用。

   定義與回應式影像資料庫搭配使用的影像預設集時，請勿使用任何會影響影像大小的設定，例如`wid=`、`hei=`或`scl=`。 請勿在影像預設集中指定任何大小欄位。 請改為保留為空白值。
1. 將資料庫JavaScript檔案新增至您的網頁。

   在可以使用資料庫API之前，請確定您已包含`responsive_image.js`。 此JavaScript檔案位於標準IS-Viewers部署的`libs/`子資料夾中：

   `<s7viewers_root>/libs/responsive_image.js`
1. 設定現有影像。

   程式庫會從正在使用的影像例項讀取某些組態屬性。 在為此類影像呼叫`s7responsiveImage` API函式之前定義屬性。

   也建議您將現有的影像URL放入`data-src`屬性中。 然後，設定現有的`src`屬性，將1x1 GIF影像編碼為資料URI。 如此一來，可減少網頁在載入時傳送的HTTP要求數目。 但是請注意，如果需要SEO （搜尋引擎最佳化），最好在影像執行個體上設定`title`屬性。

   以下範例說明如何定義影像的`data-breakpoints`屬性，以及如何使用編碼為資料URI的1x1 GIF：

   ```
   <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
   ```

1. 呼叫資料庫所管理之每個影像執行個體的`s7responsiveImage` API函式。

   呼叫資料庫所管理之每個影像執行個體的`s7responsiveImage` API函式。 進行這類呼叫後，資料庫會根據網頁版面中`IMG`元素的執行階段大小和裝置熒幕的密度，將原始影像取代為從「影像伺服」下載的影像。

   下列程式碼是在影像上呼叫`s7responsiveImage` API函式的範例，假設`responsiveImage`是該影像的ID：

   ```
   <script type="text/javascript"> 
    s7responsiveImage(document.getElementById("responsiveImage")); 
   </script>
   ```

## 範例 {#example-0509a0dd2a8e4fd58b5d39a0df47bd87}

資料庫支援同時使用網頁上的許多影像執行個體。 因此，請針對您想要程式庫管理的每個影像，重複上述步驟1和2。

網頁應負責設定影像元素的樣式，使其大小可彈性調整。 Responsive影像資料庫本身不會區別固定大小和「流動」影像。 如果套用至固定大小的影像，則只會載入新影像一次。

下列程式碼為簡單網頁的完整範例，此網頁具有由Responsive Image資料庫管理的單一Fluid影像。 此範例包含額外的CSS樣式，可讓影像「回應」網頁瀏覽器視窗大小：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
 <head> 
  <style type="text/css"> 
  .container { 
   width: 50%; 
  } 
  .fluidimage { 
   max-width: 100%; 
  } 
  </style> 
 </head> 
 <body> 
  <div class="container"> 
   <img id="responsiveImage" src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="200,400,600,800" class="fluidimage"> 
  </div> 
  <script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/libs/responsive_image.js"></script> 
  <script type="text/javascript"> 
   s7responsiveImage(document.getElementById("responsiveImage")); 
  </script> 
 </body> 
</html>
```

**使用智慧型裁切**

AEM 6.4和Dynamic Media Viewers 5.9提供兩種智慧型裁切模式：

* **手動** — 使用者定義的中斷點與對應的影像服務命令定義於影像元素的屬性內。
* **智慧型裁切** — 系統會自動從傳遞伺服器擷取運算智慧型裁切轉譯。 最佳轉譯是使用影像元素的執行階段大小來選取。

若要使用智慧型裁切模式，請將`data-mode`屬性設定為`smart crop`。 例如: 

```html {.line-numbers}
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

當中斷點變更時，關聯的影像元素會在執行階段傳送`s7responsiveViewer`事件。

```javascript {.line-numbers}
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
