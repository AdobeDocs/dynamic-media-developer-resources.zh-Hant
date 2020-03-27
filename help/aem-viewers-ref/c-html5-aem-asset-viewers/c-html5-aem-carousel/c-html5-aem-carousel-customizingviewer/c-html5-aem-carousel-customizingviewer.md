---
description: 建立自訂CSS即可完成轉盤檢視器的所有視覺化自訂和大部分行為自訂。
keywords: responsive
seo-description: 建立自訂CSS即可完成轉盤檢視器的所有視覺化自訂和大部分行為自訂。
seo-title: 自訂轉盤檢視器
solution: Experience Manager
title: 自訂轉盤檢視器
topic: Dynamic media
uuid: a35dac3c-8785-42bf-8284-e400128f213c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 自訂轉盤檢視器{#customizing-carousel-viewer}

建立自訂CSS即可完成轉盤檢視器的所有視覺化自訂和大部分行為自訂。

建議的工作流程是為適當的檢視器取用預設的CSS檔案、將它複製到不同位置、自訂檔案，並在命令中指定自訂檔案的位 `style=` 置。

您可在下列位置找到預設的CSS檔案：

`<s7viewers_root>/etc/dam/viewers/s7viewers/html5/CarouselViewer_dotted_light.css`

檢視器提供4個現成可用的CSS檔案，以數值和虛線設定指標顯示，每個都採用「淺色」和「深色」色彩配置。 預設會使用「點狀光」版本，但是使用不同的標準CSS並設定參數，就可輕鬆切換至不同的 `SetIndicator.mode` 版本。 其他標準CSS位於下列位置：

`<s7_viewers_root>/html5/CarouselViewer_dotted_dark.css`

`<s7_viewers_root>/html5/CarouselViewer_numeric_dark.css`

`<s7_viewers_root>/html5/CarouselViewer_numeric_light.css`

自訂CSS檔案必須包含與預設的類別宣告相同。 如果省略類別宣告，檢視器將無法正常運作，因為它不提供使用者介面元素的內建預設樣式。

提供自訂CSS規則的另一種方式，是直接在網頁或連結的外部CSS規則中使用內嵌樣式。

建立自訂CSS時，請記住檢視器會將類 `.s7carouselviewer` 別指派給其容器DOM元素。 如果您使用隨命令傳遞的外部CSS檔案，請 `style=` 在CSS規 `.s7carouselviewer` 則的子體選擇器中，使用類別做為上層類別。 如果您要在網頁上新增內嵌樣式，請另外以容器DOM元素的ID來限定此選取器，如下所示：

`#<containerId>.s7carouselviewer`

## 建立互動式設計的CSS {#section-0bb49aca42d242d9b01879d5ba59d33b}

您可以針對不同的裝置，以及CSS中的內嵌大小，讓您的內容顯示方式視使用者的裝置或特定網頁版面而定。 這包括（但不限於）不同的版面、使用者介面元素大小和圖稿解析度。

檢視器支援兩種建立互動式設計CSS的機制：CSS標籤和標準CSS媒體查詢。 您可以單獨使用或搭配使用。

**CSS標籤**

為協助建立互動式設計的CSS，檢視器支援CSS標籤。 這些是動態指派給頂層檢視器容器元素的特殊CSS類別。 這些檢視器會根據執行時期檢視器大小和目前裝置上使用的輸入類型而定。

第一組CSS標籤包含 `.s7size_large`、 `.s7size_medium`和 `.s7size_small` 類。 它們會根據檢視器容器的執行時期區域套用。 例如，如果檢視器區域等於或大於一般案頭螢幕的大小，請使用 `.s7size_large`。 如果區域靠近一般的平板電腦裝置，請指定 `.s7size_medium`。 對於類似行動電話螢幕的區域，請使用 `.s7size_small`。 這些CSS標籤的主要用途是針對不同的螢幕和檢視器大小，建立不同的使用者介面版面。

第二組CSS標籤包含 `.s7mouseinput` 和 `.s7touchinput`。 如果目前的 `.s7touchinput` 裝置能夠進行觸控輸入，則設定CSS標籤。 否則， `.s7mouseinput` 將使用。 這些標籤主要用於針對不同的輸入類型建立具有不同螢幕大小的使用者介面輸入元素，因為通常觸控輸入需要較大的元素。

下列範例CSS將使用滑鼠輸入的系統上的按鈕大小設定為28 x 28像素，以及觸控輸入裝置上的56 x 56像素。 如果檢視器的大小更小，則會設為20 x 20像素。

```
.s7carouselviewer.s7mouseinput .s7imagemapeffect .s7icon { 
    width:28px; 
    height:28px; 
} 
.s7carouselviewer.s7touchinput .s7imagemapeffect .s7icon { 
    width:56px; 
    height:56px; 
} 
.s7carouselviewer.s7size_small .s7imagemapeffect .s7icon { 
    width:20px; 
    height:20px; 
}
```

若要定位像素密度不同的裝置，您需要使用CSS媒體查詢。 下列媒體查詢區塊將包含高密度螢幕專用的CSS:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

使用CSS標籤是建立互動式設計CSS最有彈性的方式，因為它不僅可讓您鎖定裝置螢幕大小，還可讓您鎖定實際的檢視器大小，這對互動式設計版面很有用。

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

1. 僅包含具高解析度螢幕之行動電話的特定規則。

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

## CSS精靈 {#section-9b6d8d601cb441d08214dada7bb4eddc}

許多檢視器使用者介面元素都使用點陣圖圖樣式化，並有多個不同的視覺狀態。 例如，按鈕通常至少有三種不同狀態： `up`、 `over`和 `down`。 每個狀態都需要為其指定自己的點陣圖圖稿。

使用傳統的樣式設定方法，CSS會針對使用者介面元素的每個狀態，個別參考伺服器上的個別影像檔案。 以下是用於設定縮放按鈕樣式的範例CSS:

```
.s7carouselviewer .s7imagemapeffect .s7icon { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
} 
.s7carouselviewer .s7imagemapeffect .s7icon:hover { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_over_touch.png); 
}
```

此方法的缺點是，當元素第一次互動時，一般使用者會體驗到使用者介面的閃爍或延遲回應。 發生此動作是因為新元素狀態的影像圖稿尚未下載。 此外，由於伺服器的HTTP呼叫數增加，此方法可能會對效能造成輕微的負面影響。

CSS精靈是另一種方式，可將所有元素狀態的影像圖稿結合為稱為「精靈」的單一PNG檔案。 此類「精靈」具有指定元素的所有視覺狀態，並依序放置。 當使用精靈設定使用者介面元素的樣式時，CSS中所有不同狀態都會參照相同的精靈影像。 此外， `background-position` 屬性會用於每個狀態，以指定使用哪一部分的「Sprite」影像。 您可以以任何適當的方式來建構「精靈」影像。 檢視器通常會垂直堆疊檢視器。

以下是以「精靈」為基礎的範例，說明相同作用點圖示的樣式：

```
.s7carouselviewer .s7imagemapeffect .s7icon { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
background-position: -0px -56px; width: 56px; height: 56px; 
} 
.s7carouselviewer .s7imagemapeffect .s7icon:hover { 
background-position: -0px -0px; width: 56px; height: 56px; 
}
```

## 一般樣式注意事項與建議 {#section-95855dccbbc444e79970f1aaa3260b7b}

* 使用CSS自訂檢視器使用者介面時，不支 `!IMPORTANT` 援使用規則來設定檢視器元素的樣式。 尤其是， `!IMPORTANT` 規則不應用來覆寫檢視器或檢視器SDK提供的任何預設或執行時期樣式。 其原因在於它可能會影響正確元件的行為。 您應該改用具有適當特定性的CSS選擇器來設定本「檢視器參考」指南中說明的CSS屬性。
* CSS內外部資產的所有路徑都會根據CSS位置而解析，而非檢視器HTML頁面位置。 將預設CSS複製到不同位置時，請注意此規則。 複製預設資產，或更新自訂CSS中的所有路徑。
* 點陣圖圖稿的偏好格式為PNG。
* 點陣圖圖會使用屬性指派給使用者介面 `background-image` 元素。
* 用戶介面 `width` 元素 `height` 的和屬性定義其邏輯大小。 傳遞給的點陣圖的大小不 `background-image` 會影響其邏輯大小。
* 若要使用高像素密度的高解析度螢幕（例如Retina），請指定點陣圖圖稿的大小是邏輯使用者介面元素大小的兩倍。 然後，應用該 `-webkit-background-size:contain` 屬性將背景縮小到邏輯用戶介面元素大小。
* 若要從使用者介面移除按鈕，請新增 `display:none` 至其CSS類別。
* 您可以針對CSS支援的色彩值使用各種格式。 如果您需要透明度，請使用格式 `rgba(R,G,B,A)`。 否則，您可以使用格式 `#RRGGBB`。

## 通用使用者介面元素 {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

以下是適用於視訊影像檢視器的使用者介面元素參考檔案：
