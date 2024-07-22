---
title: 主控制列
description: 主要控制列是桌上型電腦系統和平板電腦上的矩形區域，其中包含所有可用於eCatalog檢視器的使用者介面控制項（「大頁面」按鈕除外）。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 4db16599-ede0-47ae-bb5a-840655d3620b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 0%

---

# 主控制列{#main-control-bar}

主要控制列是桌上型電腦系統和平板電腦上的矩形區域，其中包含所有可用於eCatalog檢視器的使用者介面控制項（「大頁面」按鈕除外）。

在行動電話上，它仍會保留縮圖、目錄、下載、列印、我的最愛、社交分享、全熒幕和關閉按鈕。 不過，「第一頁」和「最後一頁」按鈕以及「頁面指示器」會從主控制列移除，並改為新增至次要控制列。 依預設，主要控制列會顯示在桌上型電腦系統和行動電話的檢視器區域頂端，並移至平板電腦的檢視器區域底部。 它一律會採用完整的可用檢視器寬度。 您可以變更其在CSS中的顏色、高度和垂直位置（相對於檢視器容器）。

使用下列CSS類別選取器來控制主控制列的外觀：

`.s7ecatalogviewer .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">前</span> </p> </td> 
   <td colname="col2"> <p>從檢視器頂端的位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">後</span> </p> </td> 
   <td colname="col2"> <p>從檢視器底部的位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>主要控制列的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色彩</span> </p> </td> 
   <td colname="col2"> <p>主要控制列的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**範例** — 設定高度為36畫素且位於檢視器容器頂端的灰色主控制列。

```
.s7ecatalogviewer .s7controlbar { 
 top: 0px; 
 height: 36px; 
 background-color: rgba(0, 0, 0, 0.5); 
}
```

主控制列支援選用的捲動功能。 如果檢視器寬度太小，而且空間不足，無法容納控制列中的所有按鈕預設，就會啟用檢視器。 在此情況下，控制列的右側會顯示一個雙狀態箭頭按鈕。 按一下或點選此按鈕，會根據捲動按鈕狀態，將所有控制列元素捲動至左側或右側。 此功能的主要使用案例是搭配小型熒幕且方向為直向的行動裝置。

主控制列的捲動功能已啟用，而次要控制列的捲動功能已停用。 使用下列CSS類別選取器來開啟和關閉此功能：

`.s7ecatalogviewer .s7controlbar .s7innercontrolbarcontainer`

<table id="table_C8225F38309B4099AF58AA1A815A8D55"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">位置</span> </p> </td> 
   <td colname="col2"> <p>設定為<span class="codeph">靜態</span>時，會停用捲動功能。 </p> <p>將此屬性設定為<span class="codeph">絕對</span>以啟用捲動功能。 </p> </td> 
  </tr> 
 </tbody> 
</table>

捲動按鈕會新增至特殊容器元素，以正確放置按鈕。 它可讓您設定不同於控制列背景的按鈕周圍區域樣式，以防捲動按鈕的高度小於控制列高度。

這個捲動按鈕容器的外觀是由下列CSS類別選取器所控制：

`.s7ecatalogviewer .s7controlbar .s7scrollbuttoncontainer`

<table id="table_2CDDA8A18345497EAC4749A0D64C1658"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">寬度</span> </p> </td> 
   <td colname="col2"> <p>通常應等於或大於捲動按鈕本身的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色彩</span> </p> </td> 
   <td colname="col2"> <p>容器背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

您可以透過CSS調整捲動按鈕本身的大小和外觀。

此按鈕的外觀是由下列CSS類別選取器所控制：

`.s7ecatalogviewer .s7controlbar .s7scrollleftrightbutton`

<table id="table_F61CB3F696AC4018B164082FFA7777F4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">寬度</span> </p> </td> 
   <td colname="col2"> <p>按鈕的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>按鈕的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景影像</span> </p> </td> 
   <td colname="col2"> <p>針對指定按鈕狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景位置</span> </p> </td> 
   <td colname="col2"> <p>若使用CSS拼寫，則定位在圖稿sprite內。 </p> <p>另請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援`state`和`selected`屬性選取器，它們可用來將不同的外觀元素套用至不同的按鈕狀態。 特別是，`state="selected"`對應於初始捲動按鈕狀態（當可以捲動控制列內容至左側時）。 屬性`state="default"`對應於內容一直向左捲動時的狀態，而捲動按鈕建議將其恢復為初始狀態。

按鈕工具提示可以本地化。 如需詳細資訊，請參閱[使用者介面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。

**範例** — 啟用行動電話主控列中的捲動功能。 此外，設定64 x 64畫素的捲動按鈕，針對選取或未選取的4種不同按鈕狀態，分別顯示不同影像：

```
.s7ecatalogviewer.s7size_small .s7controlbar .s7innercontrolbarcontainer { 
 position: absolute; 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollbuttoncontainer { 
 width:64px; 
 background-color: rgb(0, 0, 0); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton { 
 width:64px; 
 height:64px; 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='up'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_up_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='over'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_over_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='down'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_down_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='disabled'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_disabled_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='up'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_up_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='over'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_over_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='down'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_down_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='disabled'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_disabled_touch.png); 
}
```
