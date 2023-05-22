---
title: 使用響應映像庫
description: 要將響應映像庫添加到網頁並使用該庫管理現有映像，請完成以下步驟。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2542b9f3-c398-4dbf-afa3-1671fc4fe72a
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 0%

---

# 使用響應映像庫{#using-responsive-image-library}

要將響應映像庫添加到網頁並使用該庫管理現有映像，請完成以下步驟。

**使用響應映像庫**

1. 在Dynamic Media Classic, [建立影像預設](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/image-sizing/setting-image-presets.html#image-sizing) 以防您計畫使用帶預設的響應影像庫。

   在定義與響應影像庫一起使用的影像預設時，不要使用任何影響影像大小的設定，如 `wid=`。 `hei=`或 `scl=`。 不要在「影像預設」中指定任何大小欄位。 相反，將其保留為空值。
1. 將庫JavaScript檔案添加到網頁。

   在使用庫API之前，請確保包括 `responsive_image.js`。 此JavaScript檔案位於 `libs/` 標準IS查看器部署的子資料夾：

   `<s7viewers_root>/libs/responsive_image.js`
1. 設定現有映像。

   庫從它正在使用的映像實例中讀取某些配置屬性。 在 `s7responsiveImage` 調用API函式來獲取此映像。

   還建議將現有影像URL放入 `data-src` 屬性。 然後，設定現有 `src` 屬性，將1x1GIF影像編碼為資料URI。 這樣，可減少網頁在載入時發送的HTTP請求數。 但請注意，如果需要SEO（搜索引擎優化），最好設定 `title` 屬性。

   以下是定義 `data-breakpoints` 影像的屬性，並使用編碼為資料URI的1x1GIF:

   ```
   <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
   ```

1. 呼叫 `s7responsiveImage` 庫管理的每個映像實例的API函式。

   呼叫 `s7responsiveImage` 庫管理的每個映像實例的API函式。 在這樣的調用之後，庫根據映像服務的運行時大小，用從映像服務下載的映像替換原始映像 `IMG` 網頁佈局中的元素和設備螢幕的密度。

   以下代碼是調用的示例 `s7responsiveImage` API函式，假設 `responsiveImage` 是該影像的ID:

   ```
   <script type="text/javascript"> 
    s7responsiveImage(document.getElementById("responsiveImage")); 
   </script>
   ```

## 範例 {#example-0509a0dd2a8e4fd58b5d39a0df47bd87}

該庫支援同時處理網頁上的許多影像實例。 因此，對希望庫管理的每個映像重複上述步驟1和2。

對影像元素進行造型是網頁的責任，使其尺寸靈活。 響應影像庫本身不區分固定大小和「流體」影像。 如果應用於固定大小的影像，則只載入一次新影像。

以下代碼是普通網頁的完整示例，該網頁具有由響應影像庫管理的單個流體影像。 該示例包含額外的CSS樣式，使影像「響應」Web瀏覽器窗口大小：

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

**使用智慧裁剪**

6.4和Dynamic Media觀眾5.9中AEM提供兩種智慧裁剪模式：

* **手動**  — 用戶定義的斷點和相應的映像服務命令在映像元素的屬性中定義。
* **智慧裁剪**  — 計算的智慧裁剪格式副本自動從交付伺服器中檢索。 使用影像元素的運行時大小選擇最佳格式副本。

要使用智慧裁剪模式，請設定 `data-mode` 屬性 `smart crop`。 例如: 

```html {.line-numbers}
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

相關影像元素分配 `s7responsiveViewer` 斷點更改時的運行時事件。

```javascript {.line-numbers}
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
