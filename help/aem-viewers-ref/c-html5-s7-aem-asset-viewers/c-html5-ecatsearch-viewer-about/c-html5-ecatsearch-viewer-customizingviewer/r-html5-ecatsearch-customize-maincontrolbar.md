---
title: 主控制條
description: 主控制欄是案頭系統和平板電腦上的矩形區域，其中包含eCatalog搜尋檢視器可用的所有使用者介面控制項（大型頁面按鈕除外）。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: cee6a4d4-4099-4bc8-9d67-00a1e963a139
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '659'
ht-degree: 1%

---

# 主控制條{#main-control-bar}

主控制欄是案頭系統和平板電腦上的矩形區域，其中包含eCatalog搜尋檢視器可用的所有使用者介面控制項（大型頁面按鈕除外）。

在行動電話上，它仍會保留縮圖、目錄、下載、列印、我的最愛、社交分享、全螢幕和關閉按鈕。 不過，「第一頁」和「最後一頁」按鈕以及「頁面指示器」會從主控制欄中移除，並改為新增至次控制列。 依預設，主控制列會顯示在案頭系統和行動電話上的檢視器區域頂端，並移至平板電腦上的檢視器區域底部。 它一律會取用整個可用的檢視器寬度。 您可以相對於檢視器容器，變更其在CSS中的顏色、高度和垂直位置。

主控制欄的外觀由下列CSS類選擇器控制：

`.s7ecatalogsearchviewer .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 頂部 </span> </p> </td> 
   <td colname="col2"> <p>從檢視器頂端的位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>從檢視器底部的位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>主控制欄的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景顏色 </span> </p> </td> 
   <td colname="col2"> <p>主控制欄的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**範例**  — 設定高度為36像素且位於檢視器容器頂端的灰色主控制欄。

```
.s7ecatalogsearchviewer .s7controlbar { 
 top: 0px; 
 height: 36px; 
 background-color: rgba(0, 0, 0, 0.5); 
}
```

主控制欄支援可選的捲動功能。 如果檢視器寬度太小，且沒有足夠的空間容納控制列中所有預設的按鈕，就會啟動它。 在此情況下，控制欄的右側會顯示一個雙狀態箭頭按鈕。 按一下或點選此按鈕會根據捲動按鈕狀態，將所有控制欄元素向左或向右捲動。 此功能的主要使用案例為縱向小螢幕的行動裝置。

主控制欄已啟用捲動功能，次控制欄則停用。 使用下列CSS類選擇器開啟和關閉功能：

`.s7ecatalogsearchviewer .s7controlbar .s7innercontrolbarcontainer`

<table id="table_C8225F38309B4099AF58AA1A815A8D55"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> position </span> </p> </td> 
   <td colname="col2"> <p>設為時 <span class="codeph"> 靜態 </span> 已禁用捲動功能。 </p> <p>將此屬性設定為 <span class="codeph"> 絕對 </span> 啟用捲動功能。 </p> </td> 
  </tr> 
 </tbody> 
</table>

捲動按鈕會新增至特殊容器元素，以正確定位按鈕。 它可讓您設定按鈕周圍區域的樣式，與控制條背景的其餘部分不同，以防捲動按鈕的高度小於控制條高度。

此捲動按鈕容器的外觀由下列CSS類選擇器控制：

`.s7ecatalogsearchviewer .s7controlbar .s7scrollbuttoncontainer`

<table id="table_2CDDA8A18345497EAC4749A0D64C1658"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>通常應等於或大於捲動按鈕本身的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景顏色 </span> </p> </td> 
   <td colname="col2"> <p>容器背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

您可以透過CSS來調整捲動按鈕本身的大小和外觀。

此按鈕的外觀由下列CSS類選擇器控制：

`.s7ecatalogsearchviewer .s7controlbar .s7scrollleftrightbutton`

<table id="table_F61CB3F696AC4018B164082FFA7777F4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度 </span> </p> </td> 
   <td colname="col2"> <p>按鈕寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度 </span> </p> </td> 
   <td colname="col2"> <p>按鈕高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景 — 影像 </span> </p> </td> 
   <td colname="col2"> <p>針對指定按鈕狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置 </span> </p> </td> 
   <td colname="col2"> <p>如果使用CSS精靈，則位於圖稿精靈內。 </p> <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援 `state` 和 `selected` 屬性選取器，可用來將不同外觀套用至不同按鈕狀態。 特別是， `state="selected"` 當可以向左滾動控制欄內容時，對應於初始滾動按鈕狀態。 此 `state="default"` 對應至內容向左捲動的狀態，而捲動按鈕建議將其傳回初始狀態。

按鈕工具提示可以本地化。 請參閱 [用戶介面元素本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 以取得更多資訊。

**範例**  — 啟用行動電話主控制欄中的捲動功能。 此外，設定一個64 x 64像素的捲動按鈕，當選取或未選取時，該按鈕會針對4個不同按鈕狀態中的每個狀態顯示不同的影像：

```
.s7ecatalogsearchviewer.s7size_small .s7controlbar .s7innercontrolbarcontainer { 
 position: absolute; 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollbuttoncontainer { 
 width:64px; 
 background-color: rgb(0, 0, 0); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton { 
 width:64px; 
 height:64px; 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='up'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_up_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='over'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_over_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='down'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_down_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='disabled'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_disabled_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='up'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_up_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='over'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_over_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='down'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_down_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='disabled'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_disabled_touch.png); 
}
```
