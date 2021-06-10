---
description: 列印工具包含新增至控制列的按鈕，以及啟動工具時顯示的強制回應對話方塊。
solution: Experience Manager
title: 列印
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog搜尋
role: Developer,Business Practitioner
exl-id: 25057e72-f079-4221-91c2-760d99d30633
source-git-commit: 8b9b87328c26e0d316c9ee09c8f4407d40efab69
workflow-type: tm+mt
source-wordcount: '1477'
ht-degree: 2%

---

# 列印{#print}

列印工具包含新增至控制列的按鈕，以及啟動工具時顯示的強制回應對話方塊。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

使用以下CSS類選擇器控制打印按鈕的外觀：

```
.s7ecatalogsearchviewer .s7print
```

**打印按鈕的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊距上  </span> </p> </td> 
   <td colname="col2"> <p> 從控制欄頂端的偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左邊距  </span> </p> </td> 
   <td colname="col2"> <p> 左側的下一個按鈕的距離；如果這是行中的第一個按鈕，則控制欄的左側。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>按鈕的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>按鈕的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景 — 影像  </span> </p> </td> 
   <td colname="col2"> <p> 針對指定按鈕狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS精靈，則位於圖稿精靈內。 </p> <p>另請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援`state`屬性選擇器，可用於將不同的外觀應用於不同的按鈕狀態。

按鈕工具提示可以本地化。 如需詳細資訊，請參閱[使用者介面元素本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 。

範例 — 設定28 x 28像素的列印按鈕，並針對四個不同按鈕狀態中的每一個顯示不同的影像。

```
.s7ecatalogsearchviewer .s7print { 
margin-top: 4px; 
margin-left: 10px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7print[state='up'] { 
background-image:url(images/v2/Print_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7print[state='over'] { 
background-image:url(images/v2/Print_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7print[state='down'] { 
background-image:url(images/v2/Print_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7print[state='disabled'] { 
background-image:url(images/v2/Print_dark_disabled.png); 
}
```

使用下列CSS類別選取器來控制當對話方塊處於作用中狀態時覆蓋網頁的背景覆蓋：

```
.s7ecatalogsearchviewer .s7printdialog .s7backoverlay
```

**背面覆蓋的CSS屬性**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 不透明度  </span> </p> </td> 
   <td colname="col2"> <p> 背景覆蓋圖不透明度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景顏色  </span> </p> </td> 
   <td colname="col2"> <p>背景覆蓋圖顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例：若要將背景覆蓋圖設定為灰色且不透明度為70%:

```
.s7ecatalogsearchviewer .s7printdialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

預設情況下，強制回應對話方塊會顯示在案頭系統的畫面中央。 該對話框的定位和大小由元件管理。該對話框由以下CSS類選擇器控制：

```
.s7ecatalogsearchviewer .s7kprintdialog .s7dialog
```

**對話框的CSS屬性**

<table id="table_5272BC8EF9124018B4290356B95B5559"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊框半徑  </span> </p> </td> 
   <td colname="col2"> <p> 對話框邊框半徑。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景顏色  </span> </p> </td> 
   <td colname="col2"> <p> 對話框背景顏色； </p> </td> 
  </tr> 
 </tbody> 
</table>

範例：若要設定具有灰色背景的對話方塊：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialog { 
background-color: #dddddd; 
}
```

對話框標題由表徵圖、標題文本和關閉按鈕組成。 標題容器可透過下列CSS類別選取器控制：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader
```

**對話框標題的CSS屬性**

<table id="table_E407E844C9BD4B5DA8B5BBDE0554F9CA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填補 </span> </p> </td> 
   <td colname="col2"> <p> 頁首內容的內部邊框間距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

圖示和標題文字會包裝在另一個容器中，由下列項目控制：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader .s7dialogline
```

**對話框行的CSS屬性**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填補 </span> </p> </td> 
   <td colname="col2"> <p> 頁首圖示和標題的內邊框間距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

使用下列CSS類選擇器控制標題表徵圖：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadericon
```

**對話框標題表徵圖的CSS屬性**

<table id="table_DD4B0413721B49CE8E21B4A55BDE8F7D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度  </span> </p> </td> 
   <td colname="col2"> <p>圖示寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度  </span> </p> </td> 
   <td colname="col2"> <p>圖示高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景 — 影像  </span> </p> </td> 
   <td colname="col2"> <p>圖示影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS精靈，則位於圖稿精靈內。 </p> <p>另請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

使用下列CSS類選擇器控制標題：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadertext
```

**對話框標題文本的CSS屬性**

<table id="table_207B4B13153E425EAB38FC61F382A05F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型粗細  </span> </p> </td> 
   <td colname="col2"> <p>字型寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型大小  </span> </p> </td> 
   <td colname="col2"> <p>字型高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型系列  </span> </p> </td> 
   <td colname="col2"> <p>字型系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填補 </span> </p> </td> 
   <td colname="col2"> <p>內部文字邊框間距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

使用下列CSS類選擇器控制關閉按鈕：

```
.s7ecatalogsearchviewer .s7printdialog .s7closebutton
```

**關閉按鈕的CSS屬性**

<table id="table_FAECBC489FC442588E50E3DA0AC16DD7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 頂部 </span> </p> </td> 
   <td colname="col2"> <p> 相對於標題容器的垂直按鈕位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右側 </span> </p> </td> 
   <td colname="col2"> <p> 相對於標題容器的水準按鈕位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度  </span> </p> </td> 
   <td colname="col2"> <p>按鈕寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度  </span> </p> </td> 
   <td colname="col2"> <p>按鈕高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填補 </span> </p> </td> 
   <td colname="col2"> <p>按鈕的內邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景 — 影像  </span> </p> </td> 
   <td colname="col2"> <p>每個狀態的按鈕影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS精靈，則位於圖稿精靈內。 </p> <p>另請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援`state`屬性選擇器，可用於將不同的外觀應用於不同的按鈕狀態。

「關閉」按鈕工具提示和對話框標題可以本地化。 如需詳細資訊，請參閱[使用者介面元素本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 。

範例 — 若要設定對話方塊標題，並加上邊框間距、22 x 22像素圖示、粗體16點標題和28 x 28像素「關閉」按鈕，以從上方放置兩個像素，從對話方塊容器的右側放置兩個像素：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader { 
 padding: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgprint_cap.png"); 
    height: 22px; 
    width: 22px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

對話框頁尾由取消和發送到打印按鈕組成。 頁尾容器可透過下列CSS類別選取器控制：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter
```

**對話框頁尾的CSS屬性**

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p> 可用於以視覺方式將頁尾與對話框其餘部分分開的邊框。 </p> </td> 
  </tr> 
 </tbody> 
</table>

頁尾有一個內容器，可保留兩個按鈕。 它由下列CSS類別選取器控制：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogbuttoncontainer
```

**對話框按鈕容器的CSS屬性**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填補 </span> </p> </td> 
   <td colname="col2"> <p> 頁尾和按鈕之間的內邊框間距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

使用下列CSS類選擇器控制取消按鈕：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton
```

**對話框取消按鈕的CSS屬性**

<table id="table_3DFA90B012F345A3A2A123D6856BE08A"> 
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
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> 每個狀態的按鈕文字顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景顏色  </span> </p> </td> 
   <td colname="col2"> <p> 每個狀態的按鈕背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援`state`屬性選擇器，可用於將不同的外觀應用於不同的按鈕狀態。

使用以下CSS類選擇器控制「發送到打印」按鈕：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton
```

**對話框操作按鈕的CSS屬性**

<table id="table_91C75B2470A24DC2AD3973A91FA8B325"> 
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
   <td colname="col1"> <p> <span class="codeph"> 色彩  </span> </p> </td> 
   <td colname="col2"> <p> 每個狀態的按鈕文字顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景顏色  </span> </p> </td> 
   <td colname="col2"> <p> 每個狀態的按鈕背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援`state`屬性選擇器，可用於將不同的外觀應用於不同的按鈕狀態。

此外，這兩個按鈕共用相同的通用CSS類，這些類可以包含其他對話框按鈕相同的CSS設定：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter .s7button
```

**按鈕的CSS屬性**

<table id="table_E735E5EDFC1E4F8A962CEA533A88DD4E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型粗細  </span> </p> </td> 
   <td colname="col2"> <p>按鈕字型寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型大小  </span> </p> </td> 
   <td colname="col2"> <p>按鈕字型大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型系列  </span> </p> </td> 
   <td colname="col2"> <p>按鈕字型系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 線高  </span> </p> </td> 
   <td colname="col2"> <p> 按鈕內的文字高度。 影響垂直對齊。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 框陰影  </span> </p> </td> 
   <td colname="col2"> <p>陰影。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊距 — 右  </span> </p> </td> 
   <td colname="col2"> <p>右鍵邊距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

按鈕工具提示可翻譯。 如需詳細資訊，請參閱[使用者介面元素本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 。

示例 — 要設定一個對話框頁尾，其中「64 x 34取消」按鈕和「96 x 34發送到打印」按鈕，每個按鈕狀態的文本顏色和背景顏色不同：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton { 
 width:96px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

主對話框區域（在頁首和頁尾之間）包含對話框內容。 在所有情況下，元件會管理此區域的寬度，因此無法在CSS中設定它。 主對話框區域由以下CSS類選擇器控制：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogviewarea
```

**對話框查看區域的CSS屬性**

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度  </span> </p> </td> 
   <td colname="col2"> <p> 主對話框區域的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景顏色  </span> </p> </td> 
   <td colname="col2"> <p>主對話框區域的背景顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>外邊距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例：若要設定主對話方塊區域，使其具有自動計算的高度、10個像素邊界，並使用白色背景：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:auto; 
}
```

所有表單內容（如標籤和輸入欄位）都駐留在由以下CSS類選擇器控制的容器內：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogbody
```

**對話框主體的CSS屬性**

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填補 </span> </p> </td> 
   <td colname="col2"> <p>內部填充。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例：若要設定表單內容，應有十個像素邊框間距：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogbody { 
    padding: 10px; 
}
```

對話框表單逐行填充，每行包含表單內容的一部分（如標籤和文本輸入欄位）。 使用下列CSS類選擇器控制單一表單行：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogline
```

**對話框行的CSS屬性**

<table id="table_2CCCC71B45B444A8B9CE2894129C9C02"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填補 </span> </p> </td> 
   <td colname="col2"> <p>內線邊框間距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例：若要設定對話方塊表單，讓每行有10個像素邊框間距：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogline { 
    padding: 10px; 
}
```

對話內容區塊的大小由下列CSS類別選取器控制：

```
 .s7ecatalogsearchviewer .s7printdialog .s7dialoginputwide
```

**對話框輸入寬度的CSS屬性**

<table id="table_FFF0B02B564C443CA8713103D723C733"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度  </span> </p> </td> 
   <td colname="col2"> <p>塊寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填補 </span> </p> </td> 
   <td colname="col2"> <p>內線邊框間距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例：若要將內容區塊設為430像素寬，且底部有10像素邊框間距：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

對話框窗體中的所有靜態標籤都使用以下CSS類選擇器進行控制：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoglabel
```

此類不適合控制標籤大小或位置，因為您可以將其應用於表單用戶介面中各個位置的文本。

**對話框標籤的CSS屬性。 **

<table id="table_13C7874807314ADD83A23075ABB4C340"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型粗細  </span> </p> </td> 
   <td colname="col2"> <p>標籤字型寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型大小  </span> </p> </td> 
   <td colname="col2"> <p>標籤字型大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型系列  </span> </p> </td> 
   <td colname="col2"> <p>標籤字型系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 色彩  </span> </p> </td> 
   <td colname="col2"> <p>標籤文本顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

對話方塊標籤可以翻譯。 如需詳細資訊，請參閱[使用者介面元素本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 。

範例：若要將所有標籤設為灰色、粗體、九像素字型：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

輸入控制項會包裝到容器中，並透過下列CSS類別選取器加以控制：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoginputcontainer
```

**對話框輸入容器的CSS屬性**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 向左邊框間距  </span> </p> </td> 
   <td colname="col2"> <p>內部填充。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 從對話方塊的左側邊緣設定30像素邊框間距。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoginputcontainer { 
    padding-left: 30px; 
}
```

選項按鈕及其標題文本由以下CSS類選擇器控制：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogoption
```

**對話框選項的CSS屬性**

<table id="table_3B4D85C5A0254A17A34D57F84F8200F7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度  </span> </p> </td> 
   <td colname="col2"> <p> 帶有字幕的單選按鈕的總寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 色彩  </span> </p> </td> 
   <td colname="col2"> <p>註解文本顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

選項按鈕與其標題之間的間距由以下CSS類選擇器控制：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogoptioninput
```

**對話框選項輸入的CSS屬性**

<table id="table_BDD03247E594416D93CDF8604DCE937B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊距 — 右  </span> </p> </td> 
   <td colname="col2"> <p> 選項按鈕與其標題之間的間距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

打印範圍選擇的數值選擇器由以下CSS類選擇器控制

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogrange
```

**對話框打印範圍的CSS屬性**

<table id="table_35413C16F6B840EBBEEA17890F2A0490"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度  </span> </p> </td> 
   <td colname="col2"> <p> 數值選擇器的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊際  </span> </p> </td> 
   <td colname="col2"> <p> 數值選擇器周圍的間距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例：若要將所有選項按鈕設定為150像素寬、黑色文字、10像素間距和42像素寬的數字選取器：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogoption { 
    color: #000000; 
    width: 150px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogoption input { 
    margin-right: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogrange { 
    margin-left: 10px; 
    margin-right: 10px; 
    width: 42px; 
}
```

頁面範圍選取項目與列印版面區段之間的水準分隔線，是透過下列CSS類別選取器來控制：

```
 .s7ecatalogsearchviewer 
.s7printdialog .s7horizontaldivider
```

**水準分隔線的CSS屬性**

<table id="table_AB42F1DC92BB4946868F0A9FE86ABAA6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊框  </span> </p> </td> 
   <td colname="col2"> <p> 分隔線周圍的邊框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填補 </span> </p> </td> 
   <td colname="col2"> <p>內部填充。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度  </span> </p> </td> 
   <td colname="col2"> <p>分隔線寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊際  </span> </p> </td> 
   <td colname="col2"> <p>外邊界 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例：若要設定430像素寬的灰度分隔線，其兩側各有10像素的垂直邊框間距，頂端則有10像素的邊界：

```
.s7ecatalogsearchviewer .s7printdialog .s7horizontaldivider { 
    border-top: 1px solid #aaaaaa; 
    margin-top: 10px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 430px; 
}
```
