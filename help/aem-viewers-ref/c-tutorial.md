---
description: 檢視器SDK提供一組以JavaScript為基礎的元件，以供自訂檢視器開發使用。 檢視器是網路應用程式，可讓Dynamic MediaAdobe所提供的多媒體內容內嵌在網頁中。
solution: Experience Manager
title: 檢視器SDK教學課程
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '974'
ht-degree: 0%

---


# 檢視器SDK教學課程{#viewer-sdk-tutorial}

檢視器SDK提供一組以JavaScript為基礎的元件，以供自訂檢視器開發使用。 檢視器是網路應用程式，可讓Dynamic MediaAdobe所提供的多媒體內容內嵌在網頁中。

例如，SDK提供互動式縮放和平移功能。 它還提供360度檢視和視訊播放資產，這些資產已透過稱為「Dynamic Media經典」的後端應用程式上傳至AdobeDynamic Media。

雖然這些元件依賴HTML5功能，但其設計可在Android和Apple iOS裝置以及桌上型電腦上運作，包括Internet Explorer和更新版本。 這種體驗意味著您可以為所有支援的平台提供單一工作流程。

SDK包含UI元件，可組成檢視器內容。 您可以透過CSS和具有某種支援角色的非UI元件來設定這些元件的樣式，例如設定定義擷取和剖析或追蹤。 所有元件行為都可透過修飾元自訂，您可以透過多種方式指定，例如，在URL中以`name=value`對的形式指定。

本教學課程包含下列工作順序，以協助您建立基本的縮放檢視器：

* [從Adobe Developer Connection下載最新的檢視器SDK](c-tutorial.md#section-84dc74c9d8e24a2380b6cf8fc28d7127)
* [載入檢視器SDK](c-tutorial.md#section-98596c276faf4cf79ccf558a9f4432c6)
* [新增樣式至檢視器](c-tutorial.md#section-3783125360a1425eae5a5a334867cc32)
* [包含容器和縮放檢視](c-tutorial.md#section-1a01730663154a508b88cc40c6f35539)
* [將MediaSet和色票元件新增至檢視器](c-tutorial.md#section-02b8c21dd842400e83eae2a48ec265b7)
* [新增按鈕至檢視器](c-tutorial.md#section-1fc334fa0d2b47eb9cdad461725c07be)
* [垂直配置色票](c-tutorial.md#section-91a8829d5b5a4d45a35b7faeb097fcc9)

## 從Adobe Developer Connection下載最新的檢視器SDK {#section-84dc74c9d8e24a2380b6cf8fc28d7127}

1. 從Adobe Developer Connection[這裡](https://marketing.adobe.com/developer/devcenter/scene7/show)下載最新的檢視器SDK。

   >[!NOTE]
   >
   >您可以完成本教學課程，毋需下載檢視器SDK套件，因為SDK實際上是遠端載入的。 不過，檢視器套件包含其他範例和API參考指南，當您建立自己的檢視器時，這些範例和參考指南會有所幫助。

## 載入檢視器SDK {#section-98596c276faf4cf79ccf558a9f4432c6}

1. 首先，設定新的頁面，以開發您要建立的基本縮放檢視器。

   請將此視為啟動載入器程式碼，以設定空的SDK應用程式。 開啟您最愛的文字編輯器，並貼入下列HTML標籤：

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

   在`script`標籤中新增下列JavaScript程式碼，以初始化`ParameterManager`。 這可協助您準備在`initViewer`函式中建立和執行個體化SDK元件：

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

   將來建立任何新檢視器時，您會使用此空白範本檔案做為參考。 此範本可在本機運作，並可在從Web伺服器提供時運作。

您現在會將樣式新增至檢視器。

## 將樣式新增至檢視器{#section-3783125360a1425eae5a5a334867cc32}

1. 對於您正在建立的完整頁面檢視器，您可以新增一些基本樣式。

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

## 包含容器和縮放檢視{#section-1a01730663154a508b88cc40c6f35539}

1. 加入元件`Container`和`ZoomView`以建立實際的檢視器。

   在[!DNL Utils.js]指令碼載入後，將以下`include`語句插入`<head>`元素的底部：

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

1. 現在，請建立變數以參考各種SDK元件。

   將下列變數新增至主要匿名函式的頂端，位於`s7sdk.Util.init()`的正上方：

   ```
   var container, zoomView;
   ```

1. 在`initViewer`函式內插入下列項目，以定義某些修飾元並執行個體化個別元件：

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

1. 預覽頁面，讓您查看已建立的內容。 您的頁面將如下所示：

   ![](assets/viewer-1.jpg)

您現在會將`MediaSet`和`Swatches`元件新增至檢視器。

## 將MediaSet和色票元件新增至檢視器{#section-02b8c21dd842400e83eae2a48ec265b7}

1. 若要讓使用者能夠從一組影像中選取影像，您可以新增元件`MediaSet`和`Swatches`。

   新增下列SDK包括：

   ```
   s7sdk.Util.lib.include('s7sdk.set.MediaSet'); 
   s7sdk.Util.lib.include('s7sdk.set.Swatches');
   ```

1. 使用下列項目更新變數清單：

   ```
   var mediaSet, container, zoomView, swatches;
   ```

1. 在`initViewer`函式中實例化`MediaSet`和`Swatches`元件。

   請務必在`ZoomView`和`Container`元件後實例化`Swatches`實例，否則堆疊順序會隱藏`Swatches`:

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

   請注意，色票位於檢視器的左下方。 若要讓色票取得整個檢視器寬度，請新增呼叫，讓使用者在調整瀏覽器大小時手動調整色票大小。 將下列內容新增至`resizeViewer`函式：

   ```
   swatches.resize(width, swatches.getHeight());
   ```

   您的檢視器現在看起來類似下列影像。 嘗試重新調整檢視器的瀏覽器視窗大小，並注意產生的行為。

   ![](assets/viewer-2.jpg)

您現在會將放大、縮小和縮放重設按鈕新增至檢視器。

## 新增按鈕至檢視器{#section-1fc334fa0d2b47eb9cdad461725c07be}

1. 目前，使用者只能使用點按或觸控手勢進行縮放。 因此，請新增一些基本的縮放控制按鈕至檢視器。

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

1. 現在，將下列項目新增至檔案最上方的`style`區塊，以定義按鈕的一些基本樣式：

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

1. 預覽檢視器。 其外觀如下：

   ![](assets/viewer-3.jpg)

   您現在會設定色票，讓色票在右側垂直對齊。

## 垂直配置色票{#section-91a8829d5b5a4d45a35b7faeb097fcc9}

1. 您可以直接在`ParameterManager`例項上設定修飾元。

   在`initViewer`函式頂端新增下列項目，將`Swatches`縮圖版面設為單一列：

   ```
   params.push("Swatches.tmblayout", "1,0");
   ```

1. 在`resizeViewer`內更新下列調整大小呼叫：

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

1. 預覽檢視器。 其外觀如下：

   ![](assets/viewer-4.jpg)

   您的基本縮放檢視器現在已完成。

   本檢視器教學課程涉及Dynamic Media檢視器SDK所提供的基礎。 當您使用SDK時，您可以使用各種標準元件，為目標受眾輕鬆建立豐富的檢視體驗並設定其樣式。

