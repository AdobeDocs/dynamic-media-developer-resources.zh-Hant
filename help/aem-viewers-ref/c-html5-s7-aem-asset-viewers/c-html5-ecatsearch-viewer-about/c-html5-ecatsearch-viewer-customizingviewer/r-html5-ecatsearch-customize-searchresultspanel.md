---
title: 搜尋結果面板
description: 搜尋結果面板由頂部的搜尋輸入方塊和顯示資訊性訊息或搜尋結果的主要區域組成。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: ffbbc2ae-60da-4c3d-a350-6dbcb64e189d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '938'
ht-degree: 0%

---

# 搜尋結果面板{#search-results-panel}

搜尋結果面板由頂部的搜尋輸入方塊和顯示資訊性訊息或搜尋結果的主要區域組成。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

主要檢視器區域的&#x200B;**CSS屬性**

當面板啟動時，檢視器使用者介面會以半透明填色覆蓋。 此填色的顏色和不透明度是由下列CSS類別選取器所控制：

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
   <td colname="col1"> <p> <span class="codeph">背景色彩</span> </p> </td> 
   <td colname="col2"> <p>覆蓋圖的顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">不透明度</span> </p> </td> 
   <td colname="col2"> <p>色彩的不透明度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

搜尋結果面板一律佔據所有可用的檢視器高度。 不過，您可以設定寬度。 您可以將寬度設定為絕對畫素值，這是大中型中斷點的預設設定。 或者，您可以將寬度設為100%，讓搜尋結果面板佔據整個檢視器區域。 面板寬度由下列CSS類別選取器控制：

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchresultspace
```

搜尋結果空間的&#x200B;**CSS屬性**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">寬度</span> </p> </td> 
   <td colname="col2"> <p> 搜尋結果空間的寬度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要在大中型中斷點上設定250畫素寬的搜尋結果面板，並在小型中斷點上使用完整大小的面板：

```
.s7ecatalogsearchviewer.s7size_large .s7searchpanel .s7searchresultspanel, .s7ecatalogsearchviewer.s7size_medium .s7searchpanel .s7searchresultspanel { 
 width:250px; 
} 
.s7ecatalogsearchviewer.s7size_small .s7searchpanel .s7searchresultspanel { 
 width:100%; 
}
```

搜尋結果面板的頂端專用於搜尋輸入方塊。 輸入方塊兩側的填補是由下列CSS類別選取器所控制：

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinputcontainer
```

搜尋輸入容器的&#x200B;**CSS屬性**

<table id="table_A1B96108542742DC8DCBCC9064F9E90B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">內距</span> </p> </td> 
   <td colname="col2"> <p> 輸入方塊周圍的內距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

搜尋輸入欄位由以下CSS類別選取器控制：

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinput
```

搜尋輸入欄位的&#x200B;**CSS屬性**

<table id="table_9FB5E89847BF4C889DC22AD7E842C0F7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>搜尋輸入欄位的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">左內距</span> </p> </td> 
   <td colname="col2"> <p> 輸入欄位界限和輸入文字之間的內邊距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">邊框</span> </p> </td> 
   <td colname="col2"> <p>搜尋輸入欄位的邊框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">利潤</span> </p> </td> 
   <td colname="col2"> <p>搜尋輸入欄位的邊界 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字型大小</span> </p> </td> 
   <td colname="col2"> <p>文字字型的大小。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要設定具有0畫素高度和14畫素文字字型的搜尋輸入欄位：

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinput { 
 padding-left:5px; 
 height:30px; 
 font-size:14px; 
}
```

依預設，以「外觀玻璃」形式顯示的搜尋輸入欄位左側的搜尋按鈕由以下CSS類別選取器控制：

```
 .s7ecatalogsearchviewer .s7searchpanel .s7searchinputbutton
```

搜尋輸入按鈕的&#x200B;**CSS屬性**

<table id="table_CDD818B40BB1416CB47B7C52F799DE0C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">寬度</span> </p> </td> 
   <td colname="col2"> <p>搜尋輸入按鈕的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>搜尋輸入按鈕的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景影像</span> </p> </td> 
   <td colname="col2"> <p>「外觀玻璃」圖示影像的URL。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景大小</span> </p> </td> 
   <td colname="col2"> <p>「外觀玻璃」圖示的大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">邊框</span> </p> </td> 
   <td colname="col2"> <p>搜尋輸入按鈕的邊框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">利潤</span> </p> </td> 
   <td colname="col2"> <p>搜尋輸入按鈕的邊界。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要設定具有26 x 26畫素「外觀玻璃」圖示的搜尋按鈕；具有1畫素邊框的30畫素大小：

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

第一次呼叫功能時，搜尋結果面板可能會顯示文字提示。 此外，當使用者的搜尋未傳回任何結果時，它也會顯示訊息。 在任何情況下，搜尋結果面板的主要部分都會顯示文字，並受到下列CSS類別選取器的控制：

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinfo
```

搜尋資訊的&#x200B;**CSS屬性**

<table id="table_1DF5A12A21584FCC8C25F170078FEFE6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">色彩</span> </p> </td> 
   <td colname="col2"> <p> 文字的色彩。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字型系列</span> </p> </td> 
   <td colname="col2"> <p>文字字型名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-align </span> </p> </td> 
   <td colname="col2"> <p>水準文字對齊方式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字型大小</span> </p> </td> 
   <td colname="col2"> <p>字型文字的大小。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此文字面板支援`state`屬性選取器，可用來將不同的樣式套用至不同的文字訊息。 特別是，`state='prompt'`對應於第一次呼叫面板時顯示的文字提示。 `state='results'`對應到包含搜尋點選相關資訊的文字。 最後，`state='no_results'`對應於搜尋查詢未傳回任何結果時所顯示的文字。

訊息文字可以當地語系化。 如需詳細資訊，請參閱[使用者介面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。

範例 — 若要設定使用灰色18畫素字型的文字面板：

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinfo { 
 font-size: 18px; 
 color: #696969; 
}
```

對於具有搜尋點選的頁面，搜尋結果會呈現為單一欄或單一列縮圖。 搜尋結果縮圖之間的間距由下列CSS類別選取器控制：

```
.ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumbcell
```

縮圖儲存格的&#x200B;**CSS屬性**

<table id="table_26974E509F6943BB98CBC1E4BAE62D68"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">利潤</span> </p> </td> 
   <td colname="col2"> <p> 每個縮圖周圍垂直邊界的大小。 實際縮圖間距等於為<span class="codeph"> .s7thumbcell </span>設定的上下邊界總和。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要設定十個畫素間距：

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

個別縮圖的外觀會受下列CSS類別選取器控制：

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumb
```

縮圖的&#x200B;**CSS屬性**

<table id="table_00829E44F75040A4B2AE19ACD550DA1E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">寬度</span> </p> </td> 
   <td colname="col2"> <p>縮圖的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>縮圖的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">邊框</span> </p> </td> 
   <td colname="col2"> <p>縮圖的邊框。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要設定215 x 129畫素、淺灰色預設邊框和深灰色選取邊框的縮圖：

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumb { 
 width: 215px; 
 height: 129px; 
}
```

縮圖示籤的外觀是由下列CSS類別選取器所控制：

```
 .s7ecatalogsearchviewer 
.s7searchpanel .s7swatches .s7label
```

標籤&#x200B;**的** CSS屬性

<table id="table_CA669F6AE7574FF389BF725B3F768E5E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">色彩</span> </p> </td> 
   <td colname="col2"> <p> 文字顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字型系列</span> </p> </td> 
   <td colname="col2"> <p>文字字型名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字型大小</span> </p> </td> 
   <td colname="col2"> <p>文字字型的大小。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要設定使用12畫素、灰色、Helvetica®字型的標籤：

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7label { 
 font-family: Helvetica,sans-serif; 
 color: #4c4c4c; 
 font-size: 12px; 
}
```

在使用滑鼠輸入的系統上，搜尋結果面板底部會顯示兩個捲動按鈕，讓使用者捲動搜尋結果。 上下捲動按鈕的外觀是由下列CSS類別選取器所控制：

```
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton
```

無法使用CSS top、left、bottom和right屬性來定位捲動按鈕。 相反地，檢視器邏輯會自動調整位置。

上下捲動按鈕的&#x200B;**CSS屬性**

<table id="table_11063C7F428D4707A8138F17650F8F5F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">寬度</span> </p> </td> 
   <td colname="col2"> <p>捲動按鈕的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>捲動按鈕的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景影像</span> </p> </td> 
   <td colname="col2"> <p> 針對指定按鈕狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景位置</span> </p> </td> 
   <td colname="col2"> <p> 若使用CSS拼寫，則定位在圖稿sprite內。 </p> <p>另請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援`state`屬性選取器，可用來將不同的外觀元素套用至`"up"`、`"down"`、`"over"`和`"disabled"`按鈕狀態。

按鈕工具提示可本地化。 如需詳細資訊，請參閱[使用者介面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。

範例 — 若要設定125 x 35畫素的向上捲動按鈕，且每個狀態都有不同的圖稿：

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
