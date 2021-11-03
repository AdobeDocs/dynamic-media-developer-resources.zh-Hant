---
title: 自訂智慧型裁切視訊檢視器
description: 自訂智慧型裁切視訊檢視器
keywords: 回應式
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 90dc93ee-fdd0-41c9-9eef-4c9952198356
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '1264'
ht-degree: 0%

---

# 自訂智慧型裁切視訊檢視器{#customizing-smartcrop-video-viewer}

所有視覺自訂和大部分行為自訂都是透過建立自訂CSS來完成。

建議的工作流程是為適當的檢視器取用預設的CSS檔案、將其複製至不同位置、自訂，以及在 `style=` 命令。

您可以在下列位置找到預設的CSS檔案：

`<s7_viewers_root>/html5/SmartCropVideoViewer.css`

自訂CSS檔案必須包含與預設檔案相同的類別宣告。 如果省略類聲明，則查看器無法正常工作，因為它不提供用戶介面元素的內置預設樣式。

提供自訂CSS規則的替代方式，是直接在網頁或其中一個連結的外部CSS規則中使用內嵌樣式。

建立自訂CSS時，請記住，檢視器會指派 `.s7smartcropvideoviewer` 類別至其容器DOM元素。 如果您使用與 `style=` 命令，使用 `.s7smartcropvideoviewer` 類別作為CSS規則的子體選取器中的上層類別。 如果您在網頁上內嵌樣式，也可以使用容器DOM元素的ID來限定此選取器，如下所示：

`#<containerId>.s7smartcropvideoviewer`

## 建立回應式設計的CSS {#section-63e8f93ee2f14fd8bba1ce33a6870b80}

您可以在CSS中鎖定不同的裝置，讓內容的顯示方式根據使用者的裝置而有所不同。 此目標包括但不限於不同的用戶介面元素大小和圖稿解析度。

檢視器支援兩種建立回應式設計CSS的機制：CSS標籤和標準CSS媒體查詢。 您可以單獨或一起使用這兩個機制。

**CSS標籤**

為協助您建立回應式設計的CSS，檢視器支援CSS標籤，這些特殊的CSS類別會動態指派給頂層檢視器容器元素。 此分配基於運行時查看器大小和當前設備上使用的輸入類型。

第一組CSS標籤包含 `.s7size_large`, `.s7size_medium`，和 `.s7size_small` 類別。 它們會根據檢視器容器的執行階段區域套用。 也就是說，如果查看器區域等於或大於公共案頭顯示器的大小 `.s7size_large` 已使用；如果區域的大小與普通平板電腦設備接近 `.s7size_medium` 已指派。 對於類似行動電話螢幕的區域， `.s7size_small` 已設定。 這些CSS標籤的主要用途是針對不同的畫面和檢視器大小建立不同的使用者介面配置。

第二組CSS標籤包括 `.s7mouseinput` 和 `.s7touchinput`. 標籤 `.s7touchinput` 若目前裝置具有觸控輸入功能，則設為；否則， `.s7mouseinput` 中所有規則的URL區段。 這些標籤旨在為不同的輸入類型建立具有不同螢幕大小的用戶介面輸入元素，因為通常觸控輸入需要較大的元素。 如果設備同時具有滑鼠輸入和觸摸功能， `.s7touchinput` 已設定，且檢視器會呈現觸控易記的使用者介面。

下列範例CSS會將使用滑鼠輸入的系統上的播放/暫停按鈕大小設為28 x 28像素，觸控裝置上則設為56 x 56像素。 此外，如果檢視器大小變小，它會完全隱藏按鈕：

```
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton { 
    width:28px; 
    height:28px; 
} 
.s7smartcropvideoviewer.s7touchinput .s7playpausebutton { 
    width:56px; 
    height:56px; 
} 
.s7smartcropvideoviewer.s7size_small .s7playpausebutton { 
    visibility:hidden; 
}
```

若要定位像素密度不同的裝置，請使用CSS媒體查詢。 下列媒體查詢區塊將包含高密度畫面專用的CSS:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

使用CSS標籤是建立回應式設計CSS的最有彈性的方式。 此彈性不僅可讓您鎖定裝置螢幕大小，還可鎖定實際的檢視器大小，這對回應式設計頁面配置可能很實用。

使用預設的檢視器CSS檔案作為CSS標籤方法的範例。

**CSS媒體查詢**

裝置偵測也可使用純CSS媒體查詢來完成。 只有在對應裝置上執行指定媒體查詢區塊內所包含的所有項目，才會套用。

套用至行動檢視器時，請使用四個CSS媒體查詢，依下列順序在CSS中定義：

1. 僅包含所有觸控裝置的特定規則。

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) 
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

1. 僅包含具有高解析度螢幕之行動電話的特定規則。

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) and (-webkit-min-device-pixel-ratio: 1.5), 
     only screen and (device-width:720px) and (device-height:1280px) and (-webkit-device-pixel-ratio: 2), 
     only screen and (device-width:1280px) and (device-height:720px) and (-webkit-device-pixel-ratio: 2) 
   { 
   }
   ```

使用CSS媒體查詢方法時，您應使用裝置偵測來組織CSS，如下所示：

* 首先，案頭專屬區段會定義所有螢幕專用或通用的屬性。
* 其次，四個媒體查詢應依上述定義的順序進行，並提供對應裝置類型專屬的CSS規則。

不需要在每個媒體查詢中複製整個檢視器CSS。 只有指定裝置專屬的屬性會在媒體查詢中重新定義。

## CSS Sprite {#section-9b6d8d601cb441d08214dada7bb4eddc}

許多查看器用戶介面元素使用點陣圖插圖進行樣式化，並且具有多個不同的視覺狀態。 一個按鈕通常至少有三種不同的狀態，這是很好的例子：「up」、「over」和「down」。 每個狀態都需要為其指定自己的點陣圖圖稿。

透過傳統的樣式方法，CSS會針對使用者介面元素的每個狀態，在伺服器上有個別影像檔案的個別參考。 以下是全螢幕按鈕樣式的範例CSS:

```
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='up'] {  
background-image:url(images/v2/PlayButton_up.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='over'] {  
background-image:url(images/v2/PlayButton_over.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='down'] {  
background-image:url(images/v2/PlayButton_down.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='disabled'] {  
background-image:url(images/v2/PlayButton_disabled.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='up'] {  
background-image:url(images/v2/PauseButton_up.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='over'] {  
background-image:url(images/v2/PauseButton_over.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='down'] {  
background-image:url(images/v2/PauseButton_down.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='disabled'] {  
background-image:url(images/v2/PauseButton_disabled.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='up'] { 
background-image:url(images/v2/ReplayButton_up.png); 
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='over'] { 
background-image:url(images/v2/ReplayButton_over.png); 
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='down'] { 
background-image:url(images/v2/ReplayButton_down.png); 
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='disabled'] { 
background-image:url(images/v2/ReplayButton_disabled.png); 
}
```

此方法的缺點是，當元素第一次互動時，一般使用者會遇到忽隱忽現或延遲的使用者介面回應。 由於新元素狀態的影像圖稿尚未下載，因此會發生此操作。 此外，此方法可能會對效能造成輕微負面影響，因為對伺服器的HTTP呼叫數量增加。

CSS精靈是不同的方法，可將所有元素狀態的影像圖稿合併為稱為「sprite」的單一PNG檔案。 這種「sprite」具有指定元素的所有視覺狀態，且這些狀態彼此定位。 使用sprite來設計使用者介面元素的樣式時，CSS中所有不同狀態都會參照相同的sprite影像。 此外， `background-position` 屬性用於每個狀態，以指定使用「sprite」影像的哪一部分。 您可以以任何適當的方式來建構「Sprite」影像。 檢視器通常會垂直堆疊檢視器。 以下是以「sprite」為基礎的範例，說明如何從上方設定相同的全螢幕按鈕：

```
.s7smartcropvideoviewer .s7fullscreenbutton[state][selected]{ 
 background-image: url(images/v2/FullScreenButton_dark_sprite.png); 
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='up'] {  
background-position: -84px -1148px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='over'] {  
background-position: -56px -1148px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='down'] {  
background-position: -28px -1148px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='disabled'] {  
background-position: -0px -1148px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='up'] {  
background-position: -84px -1120px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='over'] {  
background-position: -56px -1120px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='down'] {  
background-position: -28px -1120px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='disabled'] {  
background-position: -0px -1120px;  
}
```

## 一般樣式附註與建議 {#section-097418bd618740bba36352629e4d88e1}

* CSS內所有外部資產的路徑都會根據CSS位置(而非檢視器HTML頁面的位置)進行解析。 將預設CSS複製到其他位置時，請記住此規則。 複製預設資產或更新自訂CSS內的路徑。
* 點陣圖稿的首選格式為PNG。
* 點陣圖圖稿使用 `background-image` 屬性。
* 此 `width` 和 `height` 用戶介面元素的屬性定義其邏輯大小。 傳遞給的點陣圖的大小 `background-image` 不會影響邏輯大小。

* 要使用高解析度螢幕（如Retina）的高像素密度，請指定點陣圖圖稿的大小是邏輯用戶介面元素大小的兩倍。 然後，套用 `-webkit-background-size:contain` 屬性，將背景縮小為邏輯使用者介面元素大小。
* 若要從使用者介面移除按鈕，請新增 `display:none` 至其CSS類別。
* CSS支援的顏色值可以使用各種格式。 如果需要透明度，請使用格式 `rgba(R,G,B,A)`. 否則，您可以使用 `#RRGGBB`.

* 使用CSS自訂檢視器使用者介面時，請使用 `!IMPORTANT` 樣式檢視器元素不支援規則。 特別是， `!IMPORTANT` 規則不應用來覆寫檢視器或檢視器SDK提供的任何預設或執行階段樣式。 原因在於，它可能會影響正確元件的行為。 相反地，您應該使用具有適當特性的CSS選取器來設定本參考指南中記錄的CSS屬性。

## 通用用戶介面元素 {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

以下是套用至智慧型裁切視訊檢視器的使用者介面元素參考檔案：
