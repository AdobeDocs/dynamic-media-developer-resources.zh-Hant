---
description: 互動式視訊檢視器的所有視覺化自訂和大部分行為自訂，都是透過建立自訂CSS來完成。
keywords: 回應式
solution: Experience Manager
title: 自訂互動式視訊檢視器
feature: Dynamic Media Classic，檢視器， SDK/API，互動式影片
role: Developer,User
exl-id: c428c3e6-81be-4708-b064-f9d794183209
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '1396'
ht-degree: 0%

---

# 自訂互動式視訊檢視器{#customizing-interactive-video-viewer}

互動式視訊檢視器的所有視覺化自訂和大部分行為自訂，都是透過建立自訂CSS來完成。

建議的工作流程是為適當的檢視器取用預設的CSS檔案、將其複製到不同位置、自訂該檔案，並在`style=`命令中指定自訂檔案的位置。

您可以在下列位置找到預設的CSS檔案：

`<s7_viewers_root>/html5/InteractiveVideoViewer_dark.css`

檢視器提供兩個現成可用的CSS檔案，用於「淺色」和「深色」色彩配置。 預設會使用「深色」版本，但使用下列標準CSS可輕鬆切換為「淺色」版本：

`<s7_viewers_root>/html5/InteractiveVideoViewer_light.css`

自訂CSS檔案必須包含與預設檔案相同的類別宣告。 如果省略類聲明，則查看器無法正常工作，因為它不提供用戶介面元素的內置預設樣式。

提供自訂CSS規則的替代方式，是直接在網頁或其中一個連結的外部CSS規則中使用內嵌樣式。

建立自訂CSS時，請記得檢視器會將`.s7interactivevideoviewer`類別指派給其容器DOM元素。 如果您使用使用`style=`命令傳遞的外部CSS檔案，請在CSS規則的子體選取器中使用`.s7interactivevideoviewer`類作為父類。 如果您要在網頁上執行內嵌樣式，請額外以容器DOM元素的ID限定此選取器，如下所示：

`#<containerId>.s7interactivevideoviewer`

## 建立回應式設計的CSS {#section-0bb49aca42d242d9b01879d5ba59d33b}

您可以鎖定不同的裝置和CSS的內嵌大小，讓內容的顯示方式根據使用者的裝置或特定網頁版面而有所不同。 這包括但不限於不同佈局、用戶介面元素大小和圖稿解析度。

檢視器支援兩種建立回應式設計CSS的機制：CSS標籤和標準CSS媒體查詢。 您可以單獨使用或一起使用。

**CSS標籤**

為協助建立回應式設計的CSS，檢視器支援CSS標籤。 這些是特殊的CSS類別，會根據執行階段檢視器大小和目前裝置上使用的輸入類型，以動態方式指派給頂層檢視器容器元素。

第一組CSS標籤包括`.s7size_large`、`.s7size_medium`和`.s7size_small`類。 它們會根據檢視器容器的執行階段區域套用。 如果查看器區域等於或大於公共案頭顯示器的大小，則使用`.s7size_large`;如果區域靠近普通平板電腦設備，則分配`.s7size_medium`。 對於類似行動電話螢幕的區域，會設定`.s7size_small`。 這些CSS標籤的主要用途是針對不同的畫面和檢視器大小建立不同的使用者介面配置。

第二組CSS標籤包含`.s7mouseinput`和`.s7touchinput`。 `.s7touchinput` 若目前裝置具有觸控輸入功能，則設為；否則， `.s7mouseinput` 會使用。這些標籤主要用於針對不同的輸入類型建立具有不同螢幕大小的使用者介面輸入元素，因為通常觸控輸入需要較大的元素。

第三組CSS標籤包含`.s7device_landscape`和`.s7device_portrait`。 `.s7device_landscape` 若觸控裝置為橫向，則設為； `.s7device_portrait` 當觸控裝置旋轉為縱向時，會使用。這些CSS標籤僅用於案頭系統。

下列範例CSS會將使用滑鼠輸入的系統上的播放/暫停按鈕大小設為28x28像素，觸控裝置上則設為56x56像素。 此外，如果檢視器大小大幅縮小，按鈕會完全隱藏：

```
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton { 
    width:28px; 
    height:28px; 
} 
.s7interactivevideoviewer.s7touchinput .s7playpausebutton { 
    width:56px; 
    height:56px; 
} 
.s7interactivevideoviewer.s7size_small .s7playpausebutton { 
    visibility:hidden; 
}
```

在下一個範例中，如果觸控裝置為縱向方向，則視訊控制列會在檢視器底部上方放置138像素，在所有其他情況下，請將它移至檢視器的最底部：

```
.s7interactivevideoviewer.s7touchinput.s7device_landscape .s7controlbar, 
.s7interactivevideoviewer.s7mouseinput .s7controlbar { 
 bottom:0px; 
} 
.s7interactivevideoviewer.s7touchinput.s7device_portrait .s7controlbar { 
 bottom:136px; 
}
```

若要定位像素密度不同的裝置，您需要使用CSS媒體查詢。 下列媒體查詢區塊將包含高密度畫面專用的CSS:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

使用CSS標籤是建立回應式設計CSS最有彈性的方式，因為它不僅可讓您鎖定裝置螢幕大小，還可鎖定實際的檢視器大小，這對回應式設計配置非常有用。

您可以使用預設的檢視器CSS檔案，作為CSS標籤方法的範例。

**CSS媒體查詢**

您也可以使用純CSS媒體查詢來完成裝置偵測。 只有在對應裝置上執行指定媒體查詢區塊內所包含的所有項目，才會套用。

套用至行動檢視器時，請依下列順序使用四個CSS媒體查詢（在您的CSS中定義）:

1. 僅包含所有觸控裝置的特定規則。

   ```
   @media only screen and (max-device-width:13.5in) and (max-device- 
   height:13.5in) and (max-device-width:799px),  
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in)  
   and (max-device-height:799px) 
   { 
   }
   ```

1. 僅包含具有高解析度螢幕的平板電腦專屬規則。

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px) and (-webkit-min-device-pixel-ratio:1.5), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) and (-webkit-min-device-pixel-ratio:1.5)  
   { 
   }
   ```

1. 僅包含所有行動電話的特定規則。

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) 
   { 
   }
   ```

1. 僅包含具有高解析度螢幕的行動電話的特定規則。

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) and (-webkit-min-device-pixel-ratio: 1.5), 
     only screen and (device-width:720px) and (device-height:1280px) and (-webkit-device-pixel-ratio: 2), 
     only screen and (device-width:1280px) and (device-height:720px) and (-webkit-device-pixel-ratio: 2) 
   { 
   }
   ```

您應使用媒體查詢方法，透過裝置感應來組織CSS，如下所示：

* 首先，案頭專屬區段定義所有特定於案頭或所有畫面通用的屬性。
* 其次，這四個媒體查詢會依上述定義的順序執行，並提供針對對應裝置類型的CSS規則。

不需要在每個媒體查詢中複製整個檢視器CSS。 只有指定裝置專屬的屬性會在媒體查詢中重新定義。

## CSS Sprite {#section-9b6d8d601cb441d08214dada7bb4eddc}

許多查看器用戶介面元素使用點陣圖插圖進行樣式化，並且具有多個不同的視覺狀態。 一個按鈕通常至少有3種不同的狀態：「up」、「over」和「down」。 每個狀態都需要為其指定自己的點陣圖圖稿。

透過傳統的樣式方法，CSS會針對使用者介面元素的每個狀態，在伺服器上有個別影像檔案的個別參考。 以下是全螢幕按鈕的樣式CSS範例：

```
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='up'] {  
background-image:url(images/v2/PlayButton_up.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='over'] {  
background-image:url(images/v2/PlayButton_over.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='down'] {  
background-image:url(images/v2/PlayButton_down.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='disabled'] {  
background-image:url(images/v2/PlayButton_disabled.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='up'] {  
background-image:url(images/v2/PauseButton_up.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='over'] {  
background-image:url(images/v2/PauseButton_over.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='down'] {  
background-image:url(images/v2/PauseButton_down.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='disabled'] {  
background-image:url(images/v2/PauseButton_disabled.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='up'] { 
background-image:url(images/v2/ReplayButton_up.png); 
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='over'] { 
background-image:url(images/v2/ReplayButton_over.png); 
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='down'] { 
background-image:url(images/v2/ReplayButton_down.png); 
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='disabled'] { 
background-image:url(images/v2/ReplayButton_disabled.png); 
}
```

此方法的缺點是，當元素第一次互動時，一般使用者會遇到忽隱忽現或延遲的使用者介面回應。 由於新元素狀態的影像圖稿尚未下載，因此會發生此操作。 此外，此方法可能會對效能造成輕微負面影響，因為對伺服器的HTTP呼叫數量增加。

CSS精靈是不同的方法，可將所有元素狀態的影像圖稿合併為稱為「sprite」的單一PNG檔案。 這種「sprite」具有指定元素的所有視覺狀態，且這些狀態彼此定位。 當使用精靈來設計使用者介面元素的樣式時，CSS中所有不同狀態都會參照相同的Sprite影像。 此外，每個狀態都使用`background-position`屬性來指定使用「sprite」影像的哪一部分。 您可以以任何適當的方式來建構「Sprite」影像。 檢視器通常會垂直堆疊檢視器。 以下是先前設計相同全螢幕按鈕的「sprite」型範例：

```
.s7interactivevideoviewer .s7fullscreenbutton[state][selected]{ 
 background-image: url(images/v2/FullScreenButton_dark_sprite.png); 
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='up'] {  
background-position: -84px -1148px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='over'] {  
background-position: -56px -1148px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='down'] {  
background-position: -28px -1148px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='disabled'] {  
background-position: -0px -1148px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='up'] {  
background-position: -84px -1120px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='over'] {  
background-position: -56px -1120px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='down'] {  
background-position: -28px -1120px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='disabled'] {  
background-position: -0px -1120px;  
}
```

## 一般樣式附註與建議 {#section-95855dccbbc444e79970f1aaa3260b7b}

* 使用CSS自訂檢視器使用者介面時，不支援使用`!IMPORTANT`規則來設定檢視器元素的樣式。 尤其是，`!IMPORTANT`規則不應用來覆寫檢視器或檢視器SDK所提供的任何預設或執行階段樣式。 原因在於，它可能會影響正確元件的行為。 相反地，您應該使用具有適當特性的CSS選取器來設定本參考指南中記錄的CSS屬性。

* CSS內所有外部資產的路徑都會根據CSS位置而非檢視器HTML頁面位置來解析。 將預設CSS複製到不同位置時，請注意此規則。 複製預設資產或更新自訂CSS內的路徑。
* 點陣圖稿的首選格式為PNG。
* 使用`background-image`屬性將點陣圖圖稿分配給用戶介面元素。
* 用戶介面元素的`width`和`height`屬性定義其邏輯大小。 傳遞給`background-image`的點陣圖的大小不影響邏輯大小。

* 要使用高解析度螢幕（如Retina）的高像素密度，請指定點陣圖圖稿的大小是邏輯用戶介面元素大小的兩倍。 然後，應用`-webkit-background-size:contain`屬性將背景縮小到邏輯用戶介面元素大小。
* 若要從使用者介面中移除按鈕，請將`display:none`新增至其CSS類別。
* CSS支援的顏色值可以使用各種格式。 如果需要透明度，請使用`rgba(R,G,B,A)`格式。 否則，可使用`#RRGGBB`格式。

## 通用用戶介面元素 {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

以下是套用至互動式視訊檢視器的使用者介面元素參考檔案：
