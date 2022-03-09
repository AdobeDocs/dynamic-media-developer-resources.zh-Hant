---
title: 查看器SDK教程
description: Viewer SDK為自定義查看器開發提供了一組基於JavaScript的元件。 觀眾是基於Web的應用程式，允許AdobeDynamic Media所服務的富媒體內容嵌入網頁。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 3a798595-6c65-4a12-983d-3cdc53830d28
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 0%

---

# 查看器SDK教程{#viewer-sdk-tutorial}

Viewer SDK為自定義查看器開發提供了一組基於JavaScript的元件。 觀眾是基於Web的應用程式，允許AdobeDynamic Media所服務的富媒體內容嵌入網頁。

例如，SDK提供互動式縮放和平移。 它還提供360°視圖和視頻回放，這些資產通過名為Dynamic Media Classic的後端應用程式上傳到AdobeDynamic Media。

儘管這些元件依賴於HTML5功能，但它們設計用於Android™和AppleiOS設備以及台式機，包括Internet Explorer和更高版本。 這種體驗意味著您可以為所有受支援的平台提供單個工作流。

SDK由構成查看器內容的UI元件組成。 您可以通過CSS和具有某種支援角色的非UI元件來設定這些元件的樣式，如設定定義提取、分析或跟蹤。 所有元件行為都可通過修改量進行自定義，您可以通過各種方式指定這些修改量，例如 `name=value` 的子菜單。

本教程包括以下任務順序，以幫助您建立基本縮放查看器：

* [從Adobe Developer Connection下載最新的查看器SDK](c-tutorial.md#section-84dc74c9d8e24a2380b6cf8fc28d7127)
* [載入查看器SDK](c-tutorial.md#section-98596c276faf4cf79ccf558a9f4432c6)
* [向查看器添加樣式](c-tutorial.md#section-3783125360a1425eae5a5a334867cc32)
* [包括容器和縮放視圖](c-tutorial.md#section-1a01730663154a508b88cc40c6f35539)
* [將MediaSet和色板元件添加到查看器](c-tutorial.md#section-02b8c21dd842400e83eae2a48ec265b7)
* [向查看器添加按鈕](c-tutorial.md#section-1fc334fa0d2b47eb9cdad461725c07be)
* [垂直配置色板](c-tutorial.md#section-91a8829d5b5a4d45a35b7faeb097fcc9)

## 從Adobe Developer Connection下載最新的查看器SDK {#section-84dc74c9d8e24a2380b6cf8fc28d7127}

1. 從Adobe Developer Connection下載最新的查看器SDK <!-- SDK NO LONGER AVAILABLE TO DOWNLOAD;DOUBLE CHECK WITH AMIT. THIS ENTIRE TOPIC IS LIKELY OBSOLETE. [here](https://marketing.adobe.com/developer/devcenter/scene7/show) -->。

   >[!NOTE]
   >
   >您可以完成本教程，而無需下載Viewer SDK包，因為SDK是遠程載入的。 但是，查看器包包含其他示例和API參考指南，可幫助您建立自己的查看器。

## 載入查看器SDK {#section-98596c276faf4cf79ccf558a9f4432c6}

1. 首先，設定新頁面以開發要建立的基本縮放查看器。

   將此新頁作為Bootstrap（或載入程式），用於設定空SDK應用程式。 開啟您最喜愛的文本編輯器，並將以下HTML標籤貼上到其中：

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
       <head> 
           <meta http-equiv="Content-Type" content="text/html; charset=utf-8" /> 
           <meta name="viewport" content="user-scalable=no, height=device-height, width=device-width, initial-scale=1.0, maximum-scale=1.0"/> 
   
           <!-- Hiding the Safari on iPhone OS UI components --> 
           <meta name="apple-mobile-web-app-capable" content="yes"/> 
           <meta name="apple-mobile-web-app-status-bar-style" content="black"/> 
           <meta name="apple-touch-fullscreen" content="no"/> 
   
           <title>Custom Viewer</title> 
   
           <!-- 
               Include Utils.js before you use any of the SDK components. This file  
               contains SDK utilities and global functions that are used to initialize the viewer and load viewer  
               components. The path to the Utils.js determines which version of the SDK that the viewer uses. You  
               can use a relative path if the viewer is deployed on one of the Adobe Dynamic Media servers and it is served  
               from the same domain. Otherwise, specify a full path to one of Adobe Dynamic Media servers that have the SDK  
               installed.  
           --> 
           <script language="javascript" type="text/javascript"      
                   src="http://s7d1.scene7.com/s7sdk/2.8/js/s7sdk/utils/Utils.js"></script> 
   
       </head> 
       <body> 
           <script language="javascript" type="text/javascript"> 
           </script>  
       </body> 
   </html>
   ```

   在 `script` 標籤以初始化 `ParameterManager`。 這樣做有助於您準備在SDK中建立和實例化元件 `initViewer` 函式：

   ```javascript {.line-numbers}
   /* We create a self-running anonymous function to encapsulate variable scope. Placing code inside such 
      a function is optional, but this prevents variables from polluting the global object.  */ 
   (function () { 
   
       // Initialize the SDK   
       s7sdk.Util.init(); 
   
       /* Create an instance of the ParameterManager component to collect components' configuration 
          that can come from a viewer preset, URL, or the HTML page itself. The ParameterManager  
          component also sends a notification s7sdk.Event.SDK_READY when all needed files are loaded 
          and the configuration parameters are processed. The other components should never be initialized 
          outside this handler. After defining the handler for the s7sdk.Event.SDK_READY event, it 
          is safe to initiate configuration initialization by calling ParameterManager.init(). */ 
       var params = new s7sdk.ParameterManager(); 
   
       /* Event handler for s7sdk.Event.SDK_READY dispatched by ParameterManager to initialize various components of  
          this viewer. */ 
       function initViewer() { 
   
       }  
   
       /* Add event handler for the s7sdk.Event.SDK_READY event dispatched by the ParameterManager when all modifiers 
          are processed and it is safe to initialize the viewer. */ 
       params.addEventListener(s7sdk.Event.SDK_READY, initViewer, false); 
   
       /* Initiate configuration initialization of ParameterManager. */ 
       params.init(); 
   
   }());
   ```

1. 將檔案另存為空模板。 您可以使用任意檔案名。

   將來在建立任何查看器時，將使用此空模板檔案作為引用。 此模板在從Web伺服器提供服務時可在本地工作。

現在將樣式添加到查看器。

## 向查看器添加樣式 {#section-3783125360a1425eae5a5a334867cc32}

1. 對於您正在建立的此完整頁面查看器，可以添加一些基本樣式。

   添加以下內容 `style` 在 `head`:

   ```html {.line-numbers}
   <style> 
       html, body { 
           width: 100%; 
           height: 100%; 
       } 
       body { 
           /* Remove any padding and margin around the edges of the browser window */ 
           padding: 0; 
           margin: 0; 
   
           /* We set overflow to hidden so that scroll bars do not flicker when resizing the window */ 
           overflow: hidden; 
       } 
   </style>
   ```

現在包括元件 `Container` 和 `ZoomView`。

## 包括容器和縮放視圖 {#section-1a01730663154a508b88cc40c6f35539}

1. 通過包括元件建立實際查看器 `Container` 和 `ZoomView`。

   插入以下內容 `include` 在 `<head>` 元素 — 在 [!DNL Utils.js] 指令碼已載入：

   ```javascript {.line-numbers}
   <!-- 
       Add an "include" statement with a related module for each component that is needed for that particular  
       viewer. Check API documentation to see a complete list of components and their modules. 
   --> 
   <script language="javascript" type="text/javascript"> 
       s7sdk.Util.lib.include('s7sdk.common.Container');  
       s7sdk.Util.lib.include('s7sdk.image.ZoomView');  
   </script>
   ```

1. 現在建立變數以引用各種SDK元件。

   將以下變數添加到主匿名函式的頂部，就在上面 `s7sdk.Util.init()`:

   ```javascript {.line-numbers}
   var container, zoomView;
   ```

1. 在 `initViewer` 函式，以便您可以定義一些修改量並實例化各個元件：

   ```javascript {.line-numbers}
   /* Modifiers can be added directly to ParameterManager instance */ 
   params.push("serverurl", "http://s7d1.scene7.com/is/image"); 
   params.push("asset", "Scene7SharedAssets/ImageSet-Views-Sample"); 
   
   /* Create a viewer container as a parent component for other user interface components that  
      are part of the viewer application and associate event handlers for resize and  
      full screen notification. The advantage of using Container as the parent is the  
      component's ability to resize and bring itself and its children to full screen. */ 
   container = new s7sdk.common.Container(null, params, "s7container"); 
   container.addEventListener(s7sdk.event.ResizeEvent.COMPONENT_RESIZE, containerResize, false); 
   
   /* Create ZoomView component */ 
   zoomView = new s7sdk.image.ZoomView("s7container", params, "myZoomView");  
   
   /* We call this to ensure all SDK components are scaled to initial conditions when viewer loads */ 
   resizeViewer(container.getWidth(), container.getHeight());
   ```

1. 要正確運行上述代碼，請添加 `containerResize` 事件處理程式和幫助程式函式：

   ```javascript {.line-numbers}
   /* Event handler for s7sdk.event.ResizeEvent.COMPONENT_RESIZE events dispatched by Container to resize 
      various view components included in this viewer. */ 
   function containerResize(event) { 
       resizeViewer(event.s7event.w, event.s7event.h); 
   } 
   
   /* Resize viewer components */ 
   function resizeViewer(width, height) { 
       zoomView.resize(width, height); 
   }
   ```

1. 預覽頁面，以便查看已建立的內容。 您的頁面應如下所示：

   ![查看器示例一個影像](assets/viewer-1.jpg)

現在添加元件 `MediaSet` 和 `Swatches` 瀏覽。

## 將MediaSet和色板元件添加到查看器 {#section-02b8c21dd842400e83eae2a48ec265b7}

1. 要讓用戶能夠從集中選擇影像，可以添加元件 `MediaSet` 和 `Swatches`。

   添加以下SDK包括：

   ```javascript {.line-numbers}
   s7sdk.Util.lib.include('s7sdk.set.MediaSet'); 
   s7sdk.Util.lib.include('s7sdk.set.Swatches');
   ```

1. 使用以下內容更新變數清單：

   ```javascript {.line-numbers}
   var mediaSet, container, zoomView, swatches;
   ```

1. 實例化 `MediaSet` 和 `Swatches` 元件 `initViewer` 的子菜單。

   確保實例化 `Swatches` 實例 `ZoomView` 和 `Container` 元件，否則堆疊順序會隱藏 `Swatches`:

   ```javascript {.line-numbers}
   // Create MediaSet to manage assets and add event listener to the NOTF_SET_PARSED event 
   mediaSet = new s7sdk.set.MediaSet(null, params, "mediaSet"); 
   
   // Add MediaSet event listener 
   mediaSet.addEventListener(s7sdk.event.AssetEvent.NOTF_SET_PARSED, onSetParsed, false); 
   
   /* create Swatches component and associate event handler for swatch selection notification */ 
   swatches = new s7sdk.set.Swatches("s7container", params, "mySwatches");   
   swatches.addEventListener(s7sdk.event.AssetEvent.SWATCH_SELECTED_EVENT, swatchSelected, false);
   ```

1. 現在添加以下事件處理程式函式：

   ```javascript {.line-numbers}
   /* Event handler for the s7sdk.event.AssetEvent.NOTF_SET_PARSED event dispatched by MediaSet to 
      assign the asset to the Swatches when parsing is complete. */ 
   function onSetParsed(e) { 
   
       // set media set for Swatches to display  
       var mediasetDesc = e.s7event.asset;  
       swatches.setMediaSet(mediasetDesc); 
   
       // select the first swatch by default  
       swatches.selectSwatch(0, true);      
   } 
   
   /* Event handler for s7sdk.event.AssetEvent.SWATCH_SELECTED_EVENT events dispatched by Swatches to switch 
      the image in the ZoomView when a different swatch is selected. */ 
   function swatchSelected(event) {     
       zoomView.setItem(event.s7event.asset);  
   }
   ```

1. 通過將以下CSS添加到 `style` 元素：

   ```CSS {.line-numbers}
   /* Align swatches to bottom of viewer */ 
   .s7swatches { 
       bottom: 0; 
       left: 0; 
       right: 0; 
       height: 150px; 
   }
   ```

1. 預覽查看器。

   注意，色板位於查看器左下角。 要使色板獲得整個查看器寬度，請添加一個調用，以便在用戶調整其瀏覽器大小時手動調整色板的大小。 將以下內容添加到 `resizeViewer` 函式：

   ```javascript {.line-numbers}
   swatches.resize(width, swatches.getHeight());
   ```

   您的查看器現在看起來與以下影像類似。 嘗試調整查看器的瀏覽器窗口大小並注意結果行為。

   ![查看器示例二圖](assets/viewer-2.jpg)

現在，將放大、縮小和縮放重置按鈕添加到查看器。

## 向查看器添加按鈕 {#section-1fc334fa0d2b47eb9cdad461725c07be}

1. 目前，用戶只能使用點擊或觸摸手勢進行縮放。 因此，向查看器添加一些基本縮放控制按鈕。

   添加以下按鈕元件：

   ```CSS {.line-numbers}
   s7sdk.Util.lib.include('s7sdk.common.Button');
   ```

1. 使用以下內容更新變數清單：

   ```javascript {.line-numbers}
   var mediaSet, container, zoomView, swatches, zoomInButton, zoomOutButton, zoomResetButton;
   ```

1. 實例化按鈕 `initViewer` 的子菜單。

   請記住，除非您指定 `z-index` 在CSS中：

   ```CSS {.line-numbers}
   /* Create Zoom In, Zoom Out and Zoom Reset buttons */ 
   zoomInButton  = new s7sdk.common.ZoomInButton("s7container", params, "zoomInBtn"); 
   zoomOutButton = new s7sdk.common.ZoomOutButton("s7container", params, "zoomOutBtn"); 
   zoomResetButton = new s7sdk.common.ZoomResetButton("s7container", params, "zoomResetBtn"); 
   
   /* Add handlers for zoom in, zoom out and zoom reset buttons inline. */ 
   zoomInButton.addEventListener("click", function() { zoomView.zoomIn(); }); 
   zoomOutButton.addEventListener("click", function() { zoomView.zoomOut(); }); 
   zoomResetButton.addEventListener("click", function() { zoomView.zoomReset(); });
   ```

1. 現在，通過將以下內容添加到 `style` 阻止：

   ```CSS {.line-numbers}
   /* define styles common to all button components and their sub-classes */ 
   .s7button { 
       position:absolute; 
       width: 28px; 
       height: 28px; 
       z-index:100; 
   } 
   
   /* position individual buttons*/ 
   .s7zoominbutton  { 
       top: 50px; 
       left: 50px; 
    } 
   .s7zoomoutbutton  { 
       top: 50px; 
       left: 80px; 
    } 
   .s7zoomresetbutton  { 
       top: 50px; 
       left: 110px; 
    }
   ```

1. 預覽查看器。 它應如下所示：

   ![查看器示例三幅影像](assets/viewer-3.jpg)

   現在配置色板，使其在右側垂直對齊。

## 垂直配置色板 {#section-91a8829d5b5a4d45a35b7faeb097fcc9}

1. 您可以直接在 `ParameterManager` 實例。

   將以下內容添加到 `initViewer` 函式，以便您可以配置 `Swatches` 將拇指佈局作為單行：

   ```javascript {.line-numbers}
   params.push("Swatches.tmblayout", "1,0");
   ```

1. 在內部更新以下調整大小呼叫 `resizeViewer`:

   ```javascript {.line-numbers}
   swatches.resize(swatches.getWidth(), height);
   ```

1. 編輯以下內容 `s7swatches` 規則 `ZoomViewer.css`:

   ```CSS {.line-numbers}
   .s7swatches { 
       top:0 ; 
       bottom: 0; 
       right: 0; 
       width: 150px; 
   }
   ```

1. 預覽查看器。 如下所示：

   ![查看器示例四個影像](assets/viewer-4.jpg)

   基本縮放查看器現已完成。

   本查看器教程介紹了Dynamic Media查看器SDK提供的基礎。 在使用SDK時，您可以使用各種標準元件來輕鬆構建和風格化目標受眾的豐富查看體驗。
