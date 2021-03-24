---
description: 搜索結果面板由頂部的搜索輸入框和顯示資訊消息或搜索結果的主區域組成。
solution: Experience Manager
title: 搜尋結果面板
feature: Dynamic Media經典，檢視器，SDK/API,eCatalog搜尋
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '935'
ht-degree: 2%

---


# 搜尋結果面板{#search-results-panel}

搜索結果面板由頂部的搜索輸入框和顯示資訊消息或搜索結果的主區域組成。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主檢視器區域的CSS屬性**

當面板啟動時，檢視器使用者介面會以半透明填色覆蓋。 此填色的色彩和不透明度由下列CSS類別選擇器控制：

```
.s7ecatalogviewer .s7searchpanel .s7backoverlay
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景色  </span> </p> </td> 
   <td colname="col2"> <p>覆蓋的顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 不透明度  </span> </p> </td> 
   <td colname="col2"> <p>顏色的不透明度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

搜尋結果面板永遠佔據所有可用的檢視器高度。 不過，您可以設定寬度。 您可以將寬度設為絕對像素值，這是中大型中斷點的預設設定。 或者，您可以將寬度設為100%，讓搜尋結果面板佔據整個檢視器區域。 面板寬度由下列CSS類別選擇器控制：

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchresultspace
```

**搜尋結果空間的CSS屬性**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 搜尋結果空間的寬度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例——要在大中小斷點上設定250像素寬的搜索結果面板，並在小斷點上使用全尺寸面板：

```
.s7ecatalogsearchviewer.s7size_large .s7searchpanel .s7searchresultspanel, .s7ecatalogsearchviewer.s7size_medium .s7searchpanel .s7searchresultspanel { 
 width:250px; 
} 
.s7ecatalogsearchviewer.s7size_small .s7searchpanel .s7searchresultspanel { 
 width:100%; 
}
```

搜尋結果面板的頂端專用於搜尋輸入方塊。 輸入方塊兩側的間距由下列CSS類別選擇器控制：

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinputcontainer
```

**搜尋輸入容器的CSS屬性**

<table id="table_A1B96108542742DC8DCBCC9064F9E90B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填補 </span> </p> </td> 
   <td colname="col2"> <p> 在輸入框周圍填充。 </p> </td> 
  </tr> 
 </tbody> 
</table>

搜尋輸入欄位由下列CSS類別選擇器控制：

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinput
```

**搜尋輸入欄位的CSS屬性**

<table id="table_9FB5E89847BF4C889DC22AD7E842C0F7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>搜尋輸入欄位的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左邊距  </span> </p> </td> 
   <td colname="col2"> <p> 輸入欄位邊界和輸入文本之間的內填充。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>搜尋輸入欄位的邊框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>搜尋輸入欄位的邊界 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型大小  </span> </p> </td> 
   <td colname="col2"> <p>文字字型大小。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例——若要設定搜尋輸入欄位，其中包含0像素高度和14像素文字字型：

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinput { 
 padding-left:5px; 
 height:30px; 
 font-size:14px; 
}
```

依預設，搜尋輸入欄位左側的搜尋按鈕會以&quot;looking glass&quot;的形式由下列CSS類別選擇器控制：

```
 .s7ecatalogsearchviewer .s7searchpanel .s7searchinputbutton
```

**搜尋輸入按鈕的CSS屬性**

<table id="table_CDD818B40BB1416CB47B7C52F799DE0C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度  </span> </p> </td> 
   <td colname="col2"> <p>搜尋輸入按鈕的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度  </span> </p> </td> 
   <td colname="col2"> <p>搜尋輸入按鈕的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景影像  </span> </p> </td> 
   <td colname="col2"> <p>「外觀玻璃」圖示影像的URL。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景大小  </span> </p> </td> 
   <td colname="col2"> <p>「外觀玻璃」圖示的大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊界  </span> </p> </td> 
   <td colname="col2"> <p>搜尋輸入按鈕的邊框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊界  </span> </p> </td> 
   <td colname="col2"> <p>搜尋輸入按鈕的邊界。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——設定一個26 x 26像素的「查找玻璃」表徵圖的搜索按鈕；大小為30像素，邊框為1像素：

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinputbutton { 
 width:30px; 
 height:30px; 
 background-size:26px 26px; 
 background-image: url(images/v2/Search_form_field.png); 
 font-size:14px; 
 border: 1px solid #696969; 
}
```

當首次調用特徵時，搜索結果面板可顯示文本提示。 當使用者的搜尋未傳回任何結果時，也會顯示訊息給使用者。 在所有情況下，文字都會出現在搜尋結果面板的主要部分，並由下列CSS類別選擇器控制：

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinfo
```

**搜尋資訊的CSS屬性**

<table id="table_1DF5A12A21584FCC8C25F170078FEFE6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> 文字的顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>文字字型名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-align  </span> </p> </td> 
   <td colname="col2"> <p>水準文字對齊。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型大小  </span> </p> </td> 
   <td colname="col2"> <p>字型文字的大小。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此文字面板支援`state`屬性選擇器，可用來將不同樣式套用至不同的文字訊息。 尤其是，`state='prompt'`對應第一次呼叫面板時顯示的文字提示；`state='results'`對應於含有搜尋點擊資訊的文字；和`state='no_results'`對應於搜尋查詢未傳回任何結果時顯示的文字。

訊息文字可以本地化。 如需詳細資訊，請參閱[使用者介面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。

範例——若要設定使用18像素灰色字型的文字面板：

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinfo { 
 font-size: 18px; 
 color: #696969; 
}
```

搜尋結果會呈現為具有搜尋點擊之頁面的單一欄或單列縮圖。 使用下列CSS類別選擇器控制搜尋結果縮圖之間的間距：

```
.ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumbcell
```

**縮圖儲存格的CSS屬性**

<table id="table_26974E509F6943BB98CBC1E4BAE62D68"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊界  </span> </p> </td> 
   <td colname="col2"> <p> 每個縮圖的垂直邊界大小。 實際縮圖間距等於為<span class="codeph"> .s7thumbcell </span>設定的上下邊界總和。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例——若要設定10像素間距：

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

個別縮圖的外觀是使用下列CSS類別選取器來控制：

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumb
```

**縮圖的CSS屬性**

<table id="table_00829E44F75040A4B2AE19ACD550DA1E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度  </span> </p> </td> 
   <td colname="col2"> <p>縮圖寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度  </span> </p> </td> 
   <td colname="col2"> <p>縮圖的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊界  </span> </p> </td> 
   <td colname="col2"> <p>縮圖邊框。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例——若要設定縮圖215 x 129像素、具有淺灰色預設邊框和深灰色選取邊框：

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumb { 
 width: 215px; 
 height: 129px; 
}
```

縮表徵圖簽的外觀由下列CSS類別選擇器控制：

```
 .s7ecatalogsearchviewer 
.s7searchpanel .s7swatches .s7label
```

**標籤的CSS屬性**

<table id="table_CA669F6AE7574FF389BF725B3F768E5E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顏色  </span> </p> </td> 
   <td colname="col2"> <p> 文字色彩. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>文字字型名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型大小  </span> </p> </td> 
   <td colname="col2"> <p>文字字型大小。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——要設定使用12像素、灰色、Helvetica字型的標籤：

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7label { 
 font-family: Helvetica,sans-serif; 
 color: #4c4c4c; 
 font-size: 12px; 
}
```

在使用滑鼠輸入的系統上，搜尋結果面板底部會出現兩個捲動按鈕，讓使用者捲動搜尋結果。 上下捲動按鈕的外觀由下列CSS類別選擇器控制：

```
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton
```

無法使用CSS上、左、下和右屬性來定位捲動按鈕。 檢視器邏輯會自動將它們定位。

**向上和向下捲動按鈕的CSS屬性**

<table id="table_11063C7F428D4707A8138F17650F8F5F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度  </span> </p> </td> 
   <td colname="col2"> <p>捲動按鈕的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度  </span> </p> </td> 
   <td colname="col2"> <p>捲動按鈕的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景影像  </span> </p> </td> 
   <td colname="col2"> <p> 為指定按鈕狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS精靈，請放在圖稿精靈內。 </p> <p>另請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS精靈</a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援`state`屬性選擇器，可用來將不同的外觀套用至`"up"`、`"down"`、`"over"`和`"disabled"`按鈕狀態。

按鈕工具提示可以本地化。 如需詳細資訊，請參閱[使用者介面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。

範例——若要設定125 x 35像素且每個狀態有不同圖稿的向上捲動按鈕：

```
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton { 
 width:125px; 
 height:35px; 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='up'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_up.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_over.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_down.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_disabled.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton { 
 width:125px; 
 height:35px; 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_up.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_over.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_down.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_disabled.png);
```

