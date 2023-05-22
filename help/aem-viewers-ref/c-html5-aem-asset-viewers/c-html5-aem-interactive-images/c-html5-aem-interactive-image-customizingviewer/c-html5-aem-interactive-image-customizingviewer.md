---
title: 自定義互動式影像查看器
description: 互動式影像查看器的所有可視化自定義和大多數行為自定義都通過建立自定義CSS來完成。
keywords: 響應
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: bb3cfe4a-ec60-4c10-82fe-9e4f8f7c586f
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '1281'
ht-degree: 0%

---

# 自定義互動式影像查看器{#customizing-interactive-image-viewer}

互動式影像查看器的所有可視化自定義和大多數行為自定義都通過建立自定義CSS來完成。

建議的工作流是為相應的查看器獲取預設CSS檔案，將其複製到其他位置，對其進行自定義，並在 `style=` 的子菜單。

預設CSS檔案可在以下位置找到：

`<s7viewers_root>/etc/dam/viewers/s7viewers/html5/InteractiveImage.css`

自定義CSS檔案必須包含與預設類聲明相同的類聲明。 如果省略了類聲明，則查看器將無法正常工作，因為它不提供用戶介面元素的內置預設樣式。

提供自定義CSS規則的替代方法是直接在網頁或連結的外部CSS規則之一中使用嵌入樣式。

建立自定義CSS時，切記查看器指定 `.s7interactiveimage` 類到其容器DOM元素。 如果使用的是與 `style=` 命令，使用 `.s7interactiveimage` 類作為CSS規則的後代選擇器中的父類。 如果要在網頁上添加嵌入樣式，還應使用容器DOM元素的ID來限定此選擇器，如下所示：

`#<containerId>.s7interactiveimage`

## 構建響應性設計的CSS {#section-0bb49aca42d242d9b01879d5ba59d33b}

根據用戶的設備或特定網頁佈局，可以將不同的設備和嵌入大小作為目標，以使內容顯示方式不同。 此技術包括但不限於不同佈局、用戶介面元素大小和圖稿解析度。

查看器支援建立響應性設計的CSS的兩種機制：CSS標籤和標準CSS媒體查詢。 您可以單獨或一起使用這些標籤或查詢。

**CSS標籤**

為幫助建立響應性設計的CSS，查看器支援CSS標籤。 這些標籤是動態分配給頂級查看器容器元素的特殊CSS類。 它們基於運行時查看器大小和當前設備上使用的輸入類型。

第一組CSS標籤包含 `.s7size_large`。 `.s7size_medium`, `.s7size_small` 類。 它們基於查看器容器的運行時區域應用。 例如，如果查看器區域等於或大於公共案頭顯示器的大小，則使用 `.s7size_large`。 如果該區域靠近普通平板電腦設備，則指定 `.s7size_medium`。 對於類似於手機螢幕的區域，請使用 `.s7size_small`。 這些CSS標籤的主要目的是為不同的螢幕和查看器大小建立不同的用戶介面佈局。

第二組CSS標籤包含 `.s7mouseinput` 和 `.s7touchinput`。 CSS標籤 `.s7touchinput` 設定。 否則， `.s7mouseinput` 的子菜單。 這些標籤主要用於為不同的輸入類型建立具有不同螢幕大小的用戶介面輸入元素，因為通常觸摸輸入需要較大的元素。

下面的示例CSS將滑鼠輸入系統上的按鈕放大大小設定為28 x 28像素，將觸摸輸入設備上的按鈕放大大小設定為56 x 56像素。 如果查看器的大小更小，則將其設定為20 x 20像素。

```
.s7interactiveimage.s7mouseinput .s7imagemapeffect .s7icon { 
    width:28px; 
    height:28px; 
} 
.s7interactiveimage.s7touchinput .s7imagemapeffect .s7icon { 
    width:56px; 
    height:56px; 
} 
.s7interactiveimage.s7size_small .s7imagemapeffect .s7icon { 
    width:20px; 
    height:20px; 
}
```

要針對具有不同像素密度的設備，必須使用CSS媒體查詢。 以下媒體查詢塊將包含特定於高密度螢幕的CSS:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

使用CSS標籤是構建響應性設計的CSS的最靈活方法，因為它不僅允許您針對設備螢幕大小，而且可以針對實際查看器大小，這對於響應性設計佈局非常有用。

可以將預設查看器CSS檔案用作CSS標籤方法的示例。

**CSS媒體查詢**

還可以使用純CSS媒體查詢來完成設備檢測。 僅當給定媒體查詢塊在相應設備上運行時，才應用該塊中包含的所有內容。

應用到Mobile Viewers時，按下列順序使用四個CSS媒體查詢（在CSS中定義）:

1. 僅包含特定於所有觸摸設備的規則。

   ```
   @media only screen and (max-device-width:13.5in) and (max-device- 
   height:13.5in) and (max-device-width:799px),  
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in)  
   and (max-device-height:799px) 
   { 
   }
   ```

1. 僅包含針對具有高解析度螢幕的平板電腦的規則。

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px) and (-webkit-min-device-pixel-ratio:1.5), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) and (-webkit-min-device-pixel-ratio:1.5)  
   { 
   }
   ```

1. 僅包含特定於所有行動電話的規則。

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) 
   { 
   }
   ```

1. 僅包含針對具有高解析度螢幕的行動電話的特定規則。

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) and (-webkit-min-device-pixel-ratio: 1.5), 
     only screen and (device-width:720px) and (device-height:1280px) and (-webkit-device-pixel-ratio: 2), 
     only screen and (device-width:1280px) and (device-height:720px) and (-webkit-device-pixel-ratio: 2) 
   { 
   }
   ```

使用媒體查詢方法，應按如下方式組織具有設備感知功能的CSS:

* 首先，特定於案頭的部分定義所有屬性，這些屬性是特定於案頭的，或是所有螢幕通用的。
* 其次，這四個媒體查詢按上述定義的順序進行，並提供特定於相應設備類型的CSS規則。

無需在每個媒體查詢中複製整個查看器CSS。 只有特定於給定設備的屬性才會在媒體查詢中重新定義。

## CSS繁體 {#section-9b6d8d601cb441d08214dada7bb4eddc}

許多查看器用戶介面元素使用點陣圖圖稿設定樣式，並具有多個不同的可視狀態。 一個很好的例子是按鈕，它通常至少有三種不同的狀態： `up`。 `over`, `down`。 每個狀態都需要分配其自己的點陣圖圖稿。

使用經典的造型方法，CSS會針對用戶介面元素的每種狀態對伺服器上的單個影像檔案有單獨的引用。 以下是用於設定放大按鈕樣式的示例CSS:

```
.s7interactiveimage .s7imagemapeffect .s7icon { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
} 
.s7interactiveimage .s7imagemapeffect .s7icon:hover { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_over_touch.png); 
}
```

這種方法的缺點是當第一次與元件交互時終端用戶經歷閃爍或延遲的用戶介面響應。 此操作是因為尚未下載新元素狀態的影像圖稿。 此外，由於對伺服器的HTTP調用數量增加，此方法可能會對效能產生輕微的負面影響。

CSS浮雕是一種不同的方法，將所有元素狀態的影像圖稿合併到稱為「sprite」的單個PNG檔案中。 這種&quot;sprite&quot;具有給定元素的所有視覺狀態，這些狀態是一個接一個地定位的。 當使用sprite設定用戶介面元素的樣式時，CSS中所有不同狀態都引用了相同的sprite影像。 另外， `background-position` 屬性用於每個狀態，以指定使用「sprite」影像的哪一部分。 可以以任何合適的方式構造「雪碧」影像。 通常，查看器會垂直堆疊。

以下是基於「sprite」的示例，用於前面設定相同的放大按鈕的樣式：

```
.s7interactiveimage .s7imagemapeffect .s7icon { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
background-position: -0px -56px; width: 56px; height: 56px; 
} 
.s7interactiveimage .s7imagemapeffect .s7icon:hover { 
background-position: -0px -0px; width: 56px; height: 56px; 
}
```

## 一般樣式說明和建議 {#section-95855dccbbc444e79970f1aaa3260b7b}

* 使用CSS自定義查看器用戶介面時， `!IMPORTANT` 樣式查看器元素不支援規則。 特別是， `!IMPORTANT` 不應使用規則覆蓋查看器或查看器SDK提供的任何預設或運行時樣式。 其原因是它可能影響正確元件的行為。 相反，應使用具有適當特異性的CSS選擇器來設定本「查看者參考指南」中記錄的CSS屬性。
* CSS內到外部資產的所有路徑都根據CSS位置而不是查看器HTML頁位置進行解析。 將預設CSS複製到其他位置時，請注意此規則。 複製預設資產，或更新自定義CSS中的所有路徑。
* 點陣圖圖稿的首選格式為PNG。
* 點陣圖圖稿使用 `background-image` 屬性。
* 的 `width` 和 `height` 用戶介面元素的屬性定義其邏輯大小。 傳遞給的點陣圖的大小 `background-image` 不影響其邏輯大小。
* 要使用高解析度螢幕（如Retina）的高像素密度，請指定比邏輯用戶介面元素大兩倍的點陣圖圖稿。 然後，應用 `-webkit-background-size:contain` 屬性，將背景縮放到邏輯用戶介面元素大小。
* 要從用戶介面中刪除按鈕，請添加 `display:none` CSS類。
* 可以使用CSS支援的顏色值的各種格式。 如果需要透明度，請使用格式 `rgba(R,G,B,A)`。 否則，可以使用 `#RRGGBB`。

## 通用用戶介面元素 {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

以下是適用於視頻影像查看器的用戶介面元素參考文檔：
