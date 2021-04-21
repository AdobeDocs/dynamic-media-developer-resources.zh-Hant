---
description: 建立自訂CSS即可完成基本縮放檢視器的所有視覺化自訂和大部分行為自訂。
keywords: 回應
solution: Experience Manager
title: 自訂基本縮放檢視器
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '1341'
ht-degree: 0%

---


# 自訂基本縮放檢視器{#customizing-basic-zoom-viewer}

建立自訂CSS即可完成基本縮放檢視器的所有視覺化自訂和大部分行為自訂。

建議的工作流程是為適當的檢視器取用預設的CSS檔案，將它複製到不同的位置，加以自訂，然後在`style=`命令中指定自訂檔案的位置。

您可在下列位置找到預設的CSS檔案：

`<s7_viewers_root>/html5/BasicZoomViewer_light.css`

檢視器提供兩個現成可用的CSS檔案，用於「淺色」和「深色」配色。 預設會使用「淺色」版本，但您可以使用下列標準CSS來切換至「深色」版本：

`<s7_viewers_root>/html5/BasicZoomViewer_dark.css`

自訂CSS檔案必須包含與預設的類別宣告相同。 如果省略類別宣告，檢視器將無法正常運作，因為它不提供使用者介面元素的內建預設樣式。

提供自訂CSS規則的替代方式是直接在網頁或連結的外部CSS規則中使用內嵌樣式。

建立自訂CSS時，請記住檢視器會指派`.s7basiczoomviewer`類別給其容器DOM元素。 如果您使用與`style=`命令一起傳遞的外部CSS檔案，請在CSS規則的子體選擇器中使用`.s7basiczoomviewer`類別作為父類別。 如果您要在網頁上執行內嵌樣式，請另外以容器DOM元素的ID來限定此選取器，如下所示：

`#<containerId>.s7basiczoomviewer`

## 建立互動式設計CSS {#section-0bb49aca42d242d9b01879d5ba59d33b}

您可以針對不同的裝置，以及CSS中的內嵌大小，讓您的內容顯示方式視使用者的裝置或特定網頁版面而有所不同。 這包括（但不限於）不同的版面、使用者介面元素大小和圖稿解析度。

檢視器支援兩種建立互動式設計CSS的機制：CSS標籤和標準CSS媒體查詢。 您可以單獨使用或搭配使用。

**CSS標籤**

為協助建立互動式設計的CSS，檢視器支援CSS標籤。 這些是特殊的CSS類別，會根據執行時期檢視器大小和目前裝置上使用的輸入類型，動態指派給頂層檢視器容器元素。

第一組CSS標籤包括`.s7size_large`、`.s7size_medium`和`.s7size_small`類。 它們會根據檢視器容器的執行時期區域套用。 如果檢視器面積等於或大於一般案頭螢幕的大小，則使用`.s7size_large`;如果區域靠近普通平板裝置，則會指派`.s7size_medium`。 對於類似行動電話畫面的區域，則會設定`.s7size_small`。 這些CSS標籤的主要用途是針對不同的螢幕和檢視器大小，建立不同的使用者介面版面。

第二組CSS標籤包含`.s7mouseinput`和`.s7touchinput`。 `.s7touchinput` 設定為當前裝置具備觸控輸入功能時；否則， `.s7mouseinput` 將使用。這些標籤主要用於針對不同的輸入類型建立具有不同螢幕大小的使用者介面輸入元素，因為觸控輸入通常需要較大的元素。 當裝置同時具備滑鼠輸入和觸控功能時，會設定`.s7touchinput`，而檢視器會轉換適合觸控的使用者介面。

下列範例CSS將使用滑鼠輸入的系統上的按鈕大小設定為28 x 28像素，在觸控裝置上設定為56 x 56像素。 此外，如果檢視器大小變得很小，則會完全隱藏按鈕：

```
.s7basiczoomviewer.s7mouseinput .s7zoominbutton { 
    width:28px; 
    height:28px; 
} 
.s7basiczoomviewer.s7touchinput .s7zoominbutton { 
    width:56px; 
    height:56px; 
} 
.s7basiczoomviewer.s7size_small .s7zoominbutton { 
    visibility:hidden; 
}
```

若要定位像素密度不同的裝置，您需要使用CSS媒體查詢。 下列媒體查詢區塊將包含高密度螢幕專用的CSS:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

使用CSS標籤是建立互動式設計CSS最有彈性的方式，因為它不僅可讓您鎖定裝置螢幕大小，還可讓您鎖定實際的檢視器大小，這對互動式設計的版面十分有用。

您可以使用預設檢視器CSS檔案做為CSS標籤方法的範例。

**CSS媒體查詢**

您也可以使用純CSS媒體查詢來完成裝置感應。 僅當特定媒體查詢區塊在對應裝置上執行時，才會套用其中包含的所有內容。

套用至行動檢視器時，請依下列順序使用四個CSS媒體查詢（在CSS中定義）:

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

1. 僅包含高解析度螢幕行動電話的特定規則。

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) and (-webkit-min-device-pixel-ratio: 1.5), 
     only screen and (device-width:720px) and (device-height:1280px) and (-webkit-device-pixel-ratio: 2), 
     only screen and (device-width:1280px) and (device-height:720px) and (-webkit-device-pixel-ratio: 2) 
   { 
   }
   ```

使用媒體查詢方法，您應將CSS與裝置感應組織如下：

* 首先，案頭特定區段會定義所有畫面專屬或通用的屬性。
* 其次，四種媒體查詢依上述定義的順序執行，並提供特定於對應裝置類型的CSS規則。

在每個媒體查詢中，不需要複製整個檢視器CSS。 只有特定於特定裝置的屬性才會在媒體查詢中重新定義。

## CSS精靈{#section-9b6d8d601cb441d08214dada7bb4eddc}

許多檢視器使用者介面元素都使用點陣圖圖樣式化，並有多個不同的視覺狀態。 例如，按鈕通常至少有3種不同狀態：&quot;up&quot;、&quot;over&quot;和&quot;down&quot;。 每個狀態都需要為其指定自己的點陣圖圖稿。

使用傳統的樣式設定方法，CSS會針對使用者介面元素的每個狀態，個別參考伺服器上的個別影像檔案。 以下是用於設定縮放按鈕樣式的範例CSS:

```
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-image:url(images/v2/ZoomInButton_dark_up.png);  
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-image:url(images/v2/ZoomInButton_dark_over.png);  
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-image:url(images/v2/ZoomInButton_dark_down.png);  
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='disabled'] {  
background-image:url(images/v2/ZoomInButton_dark_disabled.png);  
}
```

此方法的缺點是，當元素第一次互動時，一般使用者會體驗到使用者介面的閃爍或延遲回應。 發生此動作是因為新元素狀態的影像圖稿尚未下載。 此外，由於伺服器的HTTP呼叫數增加，此方法可能會對效能造成輕微的負面影響。

CSS精靈是另一種方式，可將所有元素狀態的影像圖稿結合為稱為「精靈」的單一PNG檔案。 此類「精靈」具有指定元素的所有視覺狀態，並依序放置。 當使用精靈設定使用者介面元素的樣式時，CSS中所有不同狀態都會參照相同的精靈影像。 此外，`background-position`屬性會用於每個狀態，以指定使用&quot;sprite&quot;影像的哪一部分。 您可以以任何適當的方式來建構「精靈」影像。 檢視器通常會垂直堆疊檢視器。 以下是以「精靈」為基礎的範例，說明上方相同的放大按鈕的樣式：

```
.s7basiczoomviewer .s7zoominbutton[state]  { 
    background-image: url(images/v2/ZoomInButton_dark_sprite.png); 
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-position: -84px -560px;  
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-position: -56px -560px;  
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-position: -28px -560px;  
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='disabled'] { 
background-position: -0px -560px;  
}
```

## 一般樣式注意事項與建議{#section-95855dccbbc444e79970f1aaa3260b7b}

* 使用CSS自訂檢視器使用者介面時，不支援使用`!IMPORTANT`規則來設定檢視器元素的樣式。 尤其是，`!IMPORTANT`規則不應用來覆寫檢視器或檢視器SDK提供的任何預設或執行時期樣式。 其原因在於，它可能會影響正確組分的行為。 您應該改用具有適當特殊性的CSS選擇器來設定本參考指南中說明的CSS屬性。
* CSS內外部資產的所有路徑都會根據CSS位置而解析，而非檢視器HTML頁面位置。 將預設CSS複製到不同位置時，請注意此規則。 複製預設資產，或更新自訂CSS中的路徑。
* 點陣圖圖稿的偏好格式為PNG。
* 使用`background-image`屬性將點陣圖圖稿分配給用戶介面元素。
* 用戶介面元素的`width`和`height`屬性定義其邏輯大小。 傳遞給`background-image`的點陣圖的大小不會影響邏輯大小。
* 若要使用高像素密度的高解析度螢幕（例如Retina），請指定點陣圖圖稿的大小是邏輯使用者介面元素大小的兩倍。 然後，應用`-webkit-background-size:contain`屬性，將背景縮小到邏輯用戶介面元素大小。
* 若要從使用者介面移除按鈕，請將`display:none`新增至其CSS類別。
* 您可以針對CSS支援的色彩值使用各種格式。 如果需要透明度，請使用`rgba(R,G,B,A)`格式。 否則，可使用格式`#RRGGBB`。

## 常用用戶介面元素{#section-d6330c9be8c444aa9b2a07886e3dbc2a}

以下是適用於基本縮放檢視器的使用者介面元素參考檔案：
