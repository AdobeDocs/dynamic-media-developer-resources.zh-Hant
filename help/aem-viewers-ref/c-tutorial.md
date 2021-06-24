---
description: 檢視器SDK提供一組以JavaScript為基礎的元件，供自訂檢視器開發使用。 檢視器是網頁型應用程式，可讓AdobeDynamic Media提供的多媒體內容內嵌在網頁中。
solution: Experience Manager
title: 檢視器SDK教學課程
feature: Dynamic Media Classic，檢視器，SDK/API
role: Developer,Business Practitioner
exl-id: 3a798595-6c65-4a12-983d-3cdc53830d28
source-git-commit: e6ff4ed80b22e10fc2bd3fac0f4e39bbf5148f8e
workflow-type: tm+mt
source-wordcount: '964'
ht-degree: 0%

---

# 檢視器SDK教學課程{#viewer-sdk-tutorial}

檢視器SDK提供一組以JavaScript為基礎的元件，供自訂檢視器開發使用。 檢視器是網頁型應用程式，可讓AdobeDynamic Media提供的多媒體內容內嵌在網頁中。

例如，SDK提供互動式縮放和平移功能。 此外，還提供360°的資產檢視和視訊播放，這些資產已透過名為Dynamic Media Classic的後端應用程式上傳至AdobeDynamic Media。

雖然元件需仰賴HTML5功能，但設計上可用於Android和Apple iOS裝置以及桌上型電腦，包括Internet Explorer和更新版本。 這種體驗表示您可以為所有支援的平台提供單一工作流程。

SDK包含組成檢視器內容的UI元件。 您可以透過CSS和非UI元件來設定這些元件的樣式，這些元件具有某種支援角色，例如設定定義擷取、剖析或追蹤。 所有元件行為都可透過修飾元進行自訂，您可透過多種方式指定，例如，在URL中指定為`name=value`配對。

本教學課程包含下列工作順序，可協助您建立基本的縮放檢視器：

* [從Adobe Developer Connection下載最新的Viewer SDK](c-tutorial.md#section-84dc74c9d8e24a2380b6cf8fc28d7127)
* [載入檢視器SDK](c-tutorial.md#section-98596c276faf4cf79ccf558a9f4432c6)
* [將樣式新增至檢視器](c-tutorial.md#section-3783125360a1425eae5a5a334867cc32)
* [包括容器和縮放視圖](c-tutorial.md#section-1a01730663154a508b88cc40c6f35539)
* [將MediaSet和色票元件新增至檢視器](c-tutorial.md#section-02b8c21dd842400e83eae2a48ec265b7)
* [將按鈕新增至檢視器](c-tutorial.md#section-1fc334fa0d2b47eb9cdad461725c07be)
* [垂直配置色票](c-tutorial.md#section-91a8829d5b5a4d45a35b7faeb097fcc9)

## 從Adobe Developer Connection下載最新的Viewer SDK {#section-84dc74c9d8e24a2380b6cf8fc28d7127}

1. 從Adobe Developer Connection <!-- SDK NO LONGER AVAILABLE TO DOWNLOAD;DOUBLE CHECK WITH AMIT. THIS ENTIRE TOPIC IS LIKELY OBSOLETE. [here](https://marketing.adobe.com/developer/devcenter/scene7/show) -->下載最新的Viewer SDK。

   >[!NOTE]
   >
   >由於SDK實際上是從遠端載入，您不需要下載檢視器SDK套件即可完成本教學課程。 不過，檢視器套件包含其他範例，以及API參考指南，當您建立自己的檢視器時，這些範例和指南將有所幫助。

## 載入檢視器SDK {#section-98596c276faf4cf79ccf558a9f4432c6}

1. 首先，請設定新的頁面，以開發您要建立的基本縮放檢視器。

   將此視為引導程式（或載入器）程式碼，用來設定空的SDK應用程式。 開啟您最喜愛的文字編輯器，並將下列HTML標籤貼入其中：

   ```
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

   在`script`標籤內新增下列JavaScript程式碼，以初始化`ParameterManager`。 這可協助您準備在`initViewer`函式內建立和實例化SDK元件：

   ```
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

1. 將檔案儲存為空範本。 您可以使用任何想要的檔案名稱。

   將來建立任何新檢視器時，您將使用此空白範本檔案作為參考。 此範本可在本機，且從Web伺服器提供時運作。

您現在會將樣式新增至檢視器。

## 將樣式新增至檢視器 {#section-3783125360a1425eae5a5a334867cc32}

1. 對於您要建立的完整頁面檢視器，您可以新增一些基本樣式。

   將以下`style`塊添加到`head`的底部：

   ```
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

您現在將包含`Container`和`ZoomView`元件。

## 包括容器和縮放視圖 {#section-1a01730663154a508b88cc40c6f35539}

1. 通過包括元件`Container`和`ZoomView`建立實際查看器。

   在[!DNL Utils.js]指令碼載入後，將以下`include`陳述式插入`<head>`元素底部：

   ```
   <!-- 
       Add an "include" statement with a related module for each component that is needed for that particular  
       viewer. Check API documentation to see a complete list of components and their modules. 
   --> 
   <script language="javascript" type="text/javascript"> 
       s7sdk.Util.lib.include('s7sdk.common.Container');  
       s7sdk.Util.lib.include('s7sdk.image.ZoomView');  
   </script>
   ```

1. 現在建立變數以參考各種SDK元件。

   將下列變數新增至主要匿名函式的頂端，緊接在`s7sdk.Util.init()`上方：

   ```
   var container, zoomView;
   ```

1. 在`initViewer`函式內插入下列項目，以定義某些修飾元並實例化個別元件：

   ```
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

1. 若要正確執行上述程式碼，請新增`containerResize`事件處理常式和協助程式函式：

   ```
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

1. 預覽頁面，以便查看已建立的內容。 您的頁面將如下所示：

   ![](assets/viewer-1.jpg)

您現在會將元件`MediaSet`和`Swatches`新增至檢視器。

## 將MediaSet和色票元件新增至檢視器 {#section-02b8c21dd842400e83eae2a48ec265b7}

1. 若要讓使用者能夠從集合中選取影像，您可以新增元件`MediaSet`和`Swatches`。

   新增下列SDK包括：

   ```
   s7sdk.Util.lib.include('s7sdk.set.MediaSet'); 
   s7sdk.Util.lib.include('s7sdk.set.Swatches');
   ```

1. 使用下列項目更新變數清單：

   ```
   var mediaSet, container, zoomView, swatches;
   ```

1. 在`initViewer`函式內實例化`MediaSet`和`Swatches`元件。

   請務必在`ZoomView`和`Container`元件之後實例化`Swatches`實例，否則堆疊順序會隱藏`Swatches`:

   ```
   // Create MediaSet to manage assets and add event listener to the NOTF_SET_PARSED event 
   mediaSet = new s7sdk.set.MediaSet(null, params, "mediaSet"); 
   
   // Add MediaSet event listener 
   mediaSet.addEventListener(s7sdk.event.AssetEvent.NOTF_SET_PARSED, onSetParsed, false); 
   
   /* create Swatches component and associate event handler for swatch selection notification */ 
   swatches = new s7sdk.set.Swatches("s7container", params, "mySwatches");   
   swatches.addEventListener(s7sdk.event.AssetEvent.SWATCH_SELECTED_EVENT, swatchSelected, false);
   ```

1. 現在新增下列事件處理常式函式：

   ```
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

1. 將下列CSS新增至`style`元素，將色票置於檢視器底部：

   ```
   /* Align swatches to bottom of viewer */ 
   .s7swatches { 
       bottom: 0; 
       left: 0; 
       right: 0; 
       height: 150px; 
   }
   ```

1. 預覽檢視器。

   請注意，色票位於檢視器的左下角。 若要讓色票取得整個檢視器寬度，請新增呼叫，每當使用者重新調整瀏覽器大小時，手動調整色票大小。 將以下內容新增至`resizeViewer`函式：

   ```
   swatches.resize(width, swatches.getHeight());
   ```

   您的檢視器現在看起來類似下列影像。 嘗試調整檢視器的瀏覽器視窗大小，並注意產生的行為。

   ![](assets/viewer-2.jpg)

您現在會將放大、縮小和縮放重設按鈕新增至檢視器。

## 將按鈕新增至檢視器 {#section-1fc334fa0d2b47eb9cdad461725c07be}

1. 目前，使用者只能使用點擊或觸控手勢來縮放。 因此，請將一些基本的縮放控制按鈕新增至檢視器。

   新增下列按鈕元件：

   ```
   s7sdk.Util.lib.include('s7sdk.common.Button');
   ```

1. 使用下列項目更新變數清單：

   ```
   var mediaSet, container, zoomView, swatches, zoomInButton, zoomOutButton, zoomResetButton;
   ```

1. 實例化`initViewer`函式底部的按鈕。

   請記住，順序很重要，除非您在CSS中指定`z-index`:

   ```
   /* Create Zoom In, Zoom Out and Zoom Reset buttons */ 
   zoomInButton  = new s7sdk.common.ZoomInButton("s7container", params, "zoomInBtn"); 
   zoomOutButton = new s7sdk.common.ZoomOutButton("s7container", params, "zoomOutBtn"); 
   zoomResetButton = new s7sdk.common.ZoomResetButton("s7container", params, "zoomResetBtn"); 
   
   /* Add handlers for zoom in, zoom out and zoom reset buttons inline. */ 
   zoomInButton.addEventListener("click", function() { zoomView.zoomIn(); }); 
   zoomOutButton.addEventListener("click", function() { zoomView.zoomOut(); }); 
   zoomResetButton.addEventListener("click", function() { zoomView.zoomReset(); });
   ```

1. 現在，將下列內容新增至檔案頂端的`style`區塊，以定義按鈕的一些基本樣式：

   ```
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

1. 預覽檢視器。 如下所示：

   ![](assets/viewer-3.jpg)

   您現在將配置色票，使其在右側垂直對齊。

## 垂直配置色票 {#section-91a8829d5b5a4d45a35b7faeb097fcc9}

1. 您可以直接在`ParameterManager`例項上配置修飾元。

   在`initViewer`函式頂端新增下列項目，將`Swatches`縮圖配置設為單一列：

   ```
   params.push("Swatches.tmblayout", "1,0");
   ```

1. 更新`resizeViewer`內的以下調整大小呼叫：

   ```
   swatches.resize(swatches.getWidth(), height);
   ```

1. 在`ZoomViewer.css`中編輯以下`s7swatches`規則：

   ```
   .s7swatches { 
       top:0 ; 
       bottom: 0; 
       right: 0; 
       width: 150px; 
   }
   ```

1. 預覽檢視器。 如下所示：

   ![](assets/viewer-4.jpg)

   您的基本縮放檢視器現在已完成。

   本檢視器教學課程探討Dynamic Media檢視器SDK提供的基礎知識。 使用SDK時，您可以使用各種標準元件，輕鬆為目標對象建立豐富檢視體驗並設定其樣式。
