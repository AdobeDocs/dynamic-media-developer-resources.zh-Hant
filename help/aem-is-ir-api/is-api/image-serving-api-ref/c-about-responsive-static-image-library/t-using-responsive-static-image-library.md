---
description: 若要將互動式影像庫新增至網頁並使用程式庫管理現有影像，請完成下列步驟。
solution: Experience Manager
title: 使用互動式影像庫
topic: Dynamic Media Image Serving - Image Rendering API
translation-type: tm+mt
source-git-commit: d38df1eb4713c034727ad0eb10834dc156122beb
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 0%

---


# 使用自適應影像庫{#using-responsive-image-library}

若要將互動式影像庫新增至網頁並使用程式庫管理現有影像，請完成下列步驟。

**使用互動式影像庫**

1. 在Dynamic Media Classic中，[建立影像預設集](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/image-sizing/setting-image-presets.html#image-sizing)，以備您打算使用含預設集的互動式影像庫時使用。

   當您定義與自適應影像庫搭配使用的影像預設集時，請勿使用影響影像大小的任何設定，例如`wid=`、`hei=`或`scl=`。 請勿在「影像預設集」中指定任何大小欄位。 請改為將其保留為空白值。
1. 將程式庫JavaScript檔案新增至您的網頁。

   請務必加入`responsive_image.js`，才能使用程式庫API。 此JavaScript檔案位於標準IS-Viewer部署的`libs/`子資料夾中：

   `<s7viewers_root>/libs/responsive_image.js`
1. 設定現有影像。

   程式庫會從其使用的影像例項中讀取某些設定屬性。 在呼叫`s7responsiveImage` API函式之前定義屬性。

   建議您將現有的影像URL放入`data-src`屬性中。 然後，將現有的`src`屬性設為1x1 GIF影像編碼為「資料URI」。 這麼做會減少網頁在載入時傳送的HTTP請求數。 但請注意，如果需要SEO（搜尋引擎最佳化），最好在影像例項上設定`title`屬性。

   以下是定義影像`data-breakpoints`屬性並使用1x1 GIF編碼為資料URI的範例：

   ```
   <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
   ```

1. 針對程式庫管理的每個影像例項呼叫`s7responsiveImage` API函式。

   針對程式庫管理的每個影像例項呼叫`s7responsiveImage` API函式。 在進行此類呼叫後，程式庫會根據網頁版面中`IMG`元素的執行時期大小和裝置畫面的密度，以從「影像伺服」下載的影像來取代原始影像。

   以下程式碼是在影像上呼叫`s7responsiveImage` API函式的範例，假設`responsiveImage`是該影像的ID:

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

AEM 6.4和Dynamic Media Viewers 5.9提供兩種智慧型裁切模式：

* **手動** -用戶定義的斷點和相應的「影像服務」命令在影像元素的屬性中定義。
* **智慧型裁切** -計算的智慧型裁切轉譯會自動從傳送伺服器擷取。使用影像元素的執行時期大小來選取最佳轉譯。

要使用智慧裁切模式，請將`data-mode`屬性設定為`smart crop`。 例如：

```
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

當斷點變更時，關聯的映像元素在運行時間中調度`s7responsiveViewer`事件。

```
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
