---
description: 目錄是位於主控制列中的按鈕。 啟動後，下拉式面板會出現，並列出頁面索引和標籤。
solution: Experience Manager
title: 目錄
feature: Dynamic Media經典，檢視器，SDK/API,eCatalog
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '1068'
ht-degree: 2%

---


# 目錄{#table-of-contents}

目錄是位於主控制列中的按鈕。 啟動後，下拉式面板會出現，並列出頁面索引和標籤。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

根據配置，該清單可以包含目錄中存在的所有頁面，或僅包含已定義明確標籤的頁面。 在案頭系統上，如果清單長於可用的螢幕空間，右側會顯示捲軸。

檢視器使用者介面中目錄按鈕的位置和大小，由下列CSS類別選擇器控制：

```
.s7ecatalogviewer .s7tableofcontents
```

**目錄的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊距頂端  </span> </p> </td> 
   <td colname="col2"> <p> 與控制條頂部的偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左邊距  </span> </p> </td> 
   <td colname="col2"> <p> 到左側下一個按鈕的距離；如果這是一行中的第一個按鈕，則到控制列左側的距離。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 目錄按鈕的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> 目錄按鈕的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景影像  </span> </p> </td> 
   <td colname="col2"> <p> 為指定按鈕狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS精靈，請放在圖稿精靈內。 </p> <p>另請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS精靈</a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援`state`屬性選擇器，可用來將不同的外觀套用至不同的按鈕狀態。

按鈕工具提示可以本地化。 如需詳細資訊，請參閱[使用者介面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。

範例——設定目錄按鈕，從下方4像素，從主控列左側43像素；大小為28 x 28像素，並會針對四種不同的按鈕狀態顯示不同的影像：

```
.s7ecatalogviewer .s7tableofcontents { 
margin-top: 4px; 
margin-left: 10px; width: 28px; 
 height: 28px; 
} 
.s7ecatalogviewer .s7tableofcontents[state='up'] { 
background-image:url(images/v2/TableOfContents_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents[state='over'] { 
background-image:url(images/v2/TableOfContents_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents[state='down'] { 
background-image:url(images/v2/TableOfContents_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents[state='disabled'] { 
background-image:url(images/v2/TableOfContents_dark_disabled.png); 
}
```

下拉式面板的外觀是使用下列CSS類別選擇器來控制：

```
 .s7ecatalogviewer .s7tableofcontents .s7panel
```

**下拉式面板的CSS屬性**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景色  </span> </p> </td> 
   <td colname="col2"> <p> 下拉式面板的背景顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 面板邊界和內容之間的內部偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 方塊陰影  </span> </p> </td> 
   <td colname="col2"> <p> 面板四周的陰影。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>無法從CSS控制下拉式面板的大小或位置；該元件以寫程式方式管理其佈局。

範例——設定下拉式面板，其中包含半透明黑色背景、內容周圍5像素邊界和下垂式陰影：

```
.s7ecatalogviewer .s7tableofcontents .s7panel { 
 background-color: rgba(0, 0, 0, 0.5); 
 margin: 5px; 
 box-shadow: 2px 2px 3px #c0c0c0; 
}
```

使用下列CSS類別選擇器來控制個別項目的外觀和感覺：

```
 .s7ecatalogviewer .s7tableofcontents .s7panel .s7item
```

**項目的CSS屬性**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>字型名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型大小  </span> </p> </td> 
   <td colname="col2"> <p>字型大小. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度  </span> </p> </td> 
   <td colname="col2"> <p>項目的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填補 </span> </p> </td> 
   <td colname="col2"> <p>內部填補。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>下拉式清單項目支援`state`屬性選擇器，可用來套用不同的面板以暫留和選取的項目狀態。

範例——設定下拉式項目，其字型為14像素，高19像素。 項目在暫留時具有深灰色背景，在選取時具有淺灰色背景：

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7item { 
font-family: Helvetica,sans-serif; 
font-size: 14px; 
height: 19px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7panel .s7item[state="over"] { 
background-color: rgb(102, 102, 102); 
} 
.s7ecatalogviewer .s7tableofcontents .s7panel .s7item[state="selected"] { 
background-color: rgb(178, 178, 178); 
}
```

顯示頁面索引的元素會使用下列CSS類別選擇器加以控制：

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7index
```

**頁面索引的CSS屬性**

<table id="table_FAA5072E4AAC48F4BE00B05D87FD9827"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 最小寬度  </span> </p> </td> 
   <td colname="col2"> <p> 最小元素寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 最大寬度  </span> </p> </td> 
   <td colname="col2"> <p> 元素寬度上限。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右邊填充  </span> </p> </td> 
   <td colname="col2"> <p> 頁面索引和頁面標籤之間的距離。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>您可以透過為`s7index` CSS類別設定`display:none`，完全隱藏頁面索引。

範例1 —— 在右側設定最小寬度為40像素、最大寬度為70像素和5像素邊界的頁面索引：

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7index { 
max-width: 70px; 
min-width: 40px; 
padding-right: 5px; 
}
```

範例2 —— 隱藏頁面索引：

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7index { 
display: none; 
}
```

頁面標籤由下列CSS類別選擇器控制：

```
 .s7ecatalogviewer .s7tableofcontents .s7panel .s7label
```

**頁面標籤的CSS屬性**

<table id="table_A42E372D931D4F04855EE5AB5530CB12"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 最小寬度  </span> </p> </td> 
   <td colname="col2"> <p> 最小元素寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 最大寬度  </span> </p> </td> 
   <td colname="col2"> <p> 元素寬度上限。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例——設定最小寬度為40像素、最大寬度為240像素的頁面索引：

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7label { 
min-width: 40px; 
max-width: 240px; 
}
```

如果下拉式面板中的項目數量超過垂直大小，而且系統為案頭，則元件會在面板右側呈現垂直捲軸。 捲軸區域的外觀由下列CSS類別選擇器控制：

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar
```

**捲軸的CSS屬性**

<table id="table_D34A63AAE6324699ABDCC08355D33035"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度  </span> </p> </td> 
   <td colname="col2"> <p> 捲軸寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 頂部 </span> </p> </td> 
   <td colname="col2"> <p> 垂直捲軸與面板區域的頂部偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p> 垂直捲軸與面板區域底部偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右側 </span> </p> </td> 
   <td colname="col2"> <p> 水準捲軸偏離面板區域的右邊緣。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例——設定寬28像素且面板頂端、右側或底部區域無邊界的捲軸：

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar { 
 top:0px; 
 bottom:0px; 
 right:0px; 
 width:28px; 
}
```

捲軸列是頂端和底部捲軸按鈕之間的區域。 該元件自動設定軌道的位置和高度。 使用下列CSS類別選擇器控制音軌：

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolltrack
```

**捲軸的CSS屬性**

<table id="table_E49EE04B3FF64AB2948E7C09DF3EA1B7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度  </span> </p> </td> 
   <td colname="col2"> <p>音軌寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景色  </span> </p> </td> 
   <td colname="col2"> <p>音軌背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例——設定寬28像素且半透明灰色背景的捲軸列：

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolltrack { 
 width:28px; 
 background-color:rgba(102, 102, 102, 0.5); 
}
```

捲動條拇指在滾動軌道區域內垂直移動。 其垂直位置由元件邏輯控制。 不過，拇指高度不會根據內容量而動態改變。 您可以使用下列CSS類別選擇器來設定縮圖高度和其他方面：

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb
```

**捲軸縮圖的CSS屬性**

<table id="table_D8DFBC2419BD4AB3B4892AC7B599C70A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度  </span> </p> </td> 
   <td colname="col2"> <p>拇指寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度  </span> </p> </td> 
   <td colname="col2"> <p>拇指高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充頂部  </span> </p> </td> 
   <td colname="col2"> <p> 軌道頂部之間的垂直間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充底部  </span> </p> </td> 
   <td colname="col2"> <p>軌道底部之間的垂直間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景影像  </span> </p> </td> 
   <td colname="col2"> <p> 顯示給定拇指狀態的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS精靈，請放在圖稿精靈內。 </p> <p>另請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS精靈</a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Thumb支援`state`屬性選擇器，該選擇器可用於將不同的外觀應用於`up`、`down`、`over`和`disabled`拇指狀態。

範例——設定捲軸縮圖28 x 45像素、上下有10像素邊界，且每個狀態的圖稿都不同：

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb { 
 width:28px; 
 background-repeat:no-repeat; 
 background-position:center; 
 height:45px; 
 padding-top:10px; 
 padding-bottom:10px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
}
```

使用下列CSS類別選擇器來控制頂端和底部捲動按鈕的外觀：

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton
```

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton
```

無法使用CSS `top`、`left`、`bottom`和`right`屬性來定位捲動按鈕；檢視器邏輯會自動定位。

**向上和向下捲動按鈕的CSS屬性**

<table id="table_89561098E43D44C2865267687BBF38F4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度  </span> </p> </td> 
   <td colname="col2"> <p>按鈕寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度  </span> </p> </td> 
   <td colname="col2"> <p>按鈕高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景影像  </span> </p> </td> 
   <td colname="col2"> <p> 為指定按鈕狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS精靈，請放在圖稿精靈內。 </p> <p>另請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS精靈</a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>按鈕支援`state`屬性選擇器，可用來將不同的外觀套用至`up`、`down`、`over`和`disabled`按鈕狀態。

按鈕工具提示可以本地化。 如需詳細資訊，請參閱[使用者介面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。

範例——設定28 x 32像素且每種狀態有不同圖稿的捲動按鈕：

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
}
```

