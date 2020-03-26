---
description: 若要將互動式影像庫新增至網頁並使用程式庫管理現有影像，請完成下列步驟。
seo-description: 若要將互動式影像庫新增至網頁並使用程式庫管理現有影像，請完成下列步驟。
seo-title: 使用互動式影像庫
solution: Experience Manager
title: 使用互動式影像庫
topic: Scene7 Image Serving - Image Rendering API
uuid: 325cdc8d-2bfa-4f9b-bf88-51d1dcc6c495
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb

---


# 使用互動式影像庫{#using-responsive-image-library}

若要將互動式影像庫新增至網頁並使用程式庫管理現有影像，請完成下列步驟。

**使用互動式影像庫**

1. 在SPS中，建 [立影像預設集](http://help.adobe.com/en_US/scene7/using/WS2F6A1049-B41F-447d-A520-91227F9CDABF.html) ，以備您打算搭配預設集使用互動式影像庫時使用。

   當您定義與自適應影像庫搭配使用的影像預設集時，請勿使用任何會影響影像大小的設定， `wid=`例如 `hei=`、或 `scl=`。 請勿在「影像預設集」中指定任何大小欄位。 請改為將其保留為空白值。
1. 將程式庫JavaScript檔案新增至您的網頁。

   請務必先納入，才能使用程式庫API `responsive_image.js`。 此JavaScript檔案位於標準IS `libs/` 檢視器部署的子資料夾：

   `<s7viewers_root>/libs/responsive_image.js`
1. 設定現有影像。

   程式庫會從其使用的影像例項中讀取某些設定屬性。 在呼叫API函 `s7responsiveImage` 數之前，先定義屬性。

   建議您將現有的影像URL放入屬 `data-src` 性。 然後，將現有屬性設 `src` 置為1x1 GIF影像編碼為「資料URI」。 這麼做會減少網頁在載入時傳送的HTTP請求數。 但請注意，如果需要SEO（搜尋引擎最佳化），最好在影像例項 `title` 上設定屬性。

   以下是定義影像屬 `data-breakpoints` 性並使用1x1 GIF編碼為資料URI的範例：

   ```
   <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
   ```

1. 呼叫程 `s7responsiveImage` 式庫管理的每個影像例項的API函式。

   呼叫程 `s7responsiveImage` 式庫管理的每個影像例項的API函式。 在這類呼叫後，程式庫會根據網頁版面中元素的執行時期大小和裝置畫面的密度，以從「影像伺服」下載的影像來取代原始影像。 `IMG`

   以下程式碼是在影像上呼叫 `s7responsiveImage` API函式的範例，假設 `responsiveImage` 該影像是ID:

   ```
   <script type="text/javascript"> 
    s7responsiveImage(document.getElementById("responsiveImage")); 
   </script>
   ```

## 範例 {#example-0509a0dd2a8e4fd58b5d39a0df47bd87}

程式庫支援同時處理網頁上的許多影像例項。 因此，請針對您希望程式庫管理的每個影像重複上述步驟1和2。

網頁負責設定影像元素的樣式，讓其大小變得靈活。 自適應影像庫本身不會區分固定大小和「流暢」的影像。 如果套用至固定大小的影像，則只會載入新影像一次。

以下程式碼是簡單網頁的完整範例，該網頁具有由自適應影像庫管理的單一流暢影像。 此範例包含額外的CSS樣式，讓影像對網頁瀏覽器視窗大小「回應」:

```
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

AEM 6.4和Scene7檢視器5.9提供兩種智慧型裁切模式：

* **Manual** —— 用戶定義的斷點和相應的Image Service命令在影像元素的屬性中定義。
* **智慧型裁切** -計算的智慧型裁切轉譯會自動從傳送伺服器擷取。 使用影像元素的執行時期大小來選取最佳轉譯。

要使用「智慧裁切」模式，請將屬 `data-mode` 性設定為 `smart crop`。 例如：

```
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

當斷點改變時，關聯的映像元 `s7responsiveViewer` 素在運行時調度事件。

```
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
