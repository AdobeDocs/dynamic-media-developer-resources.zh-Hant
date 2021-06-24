---
description: 電子郵件共用工具包含新增至Social共用面板的按鈕，以及啟動工具時顯示的強制回應對話方塊。 按鈕的位置由Social分享工具完全管理。
solution: Experience Manager
title: 電子郵件共用
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog搜尋
role: Developer,Business Practitioner
exl-id: a879994d-2f26-4fdd-9a51-73644fc033cd
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '3041'
ht-degree: 2%

---

# 電子郵件共用{#email-share}

電子郵件共用工具包含新增至Social共用面板的按鈕，以及啟動工具時顯示的強制回應對話方塊。 按鈕的位置由Social分享工具完全管理。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

電子郵件共用按鈕的外觀由下列CSS類別選取器控制：

```
.s7ecatalogsearchviewer .s7emailshare
```

**電子郵件共用工具的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
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

您可以在其CSS類別上設定`display:none` CSS屬性，從Social共用面板中移除按鈕。

按鈕工具提示可以本地化。 如需詳細資訊，請參閱[使用者介面元素本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 。

範例：若要設定28 x 28像素的電子郵件共用按鈕，並針對四個不同按鈕狀態中的每一個顯示不同的影像。

```
.s7ecatalogsearchviewer .s7emailshare { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7emailshare[state='up'] { 
background-image:url(images/v2/EmailShare_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7emailshare[state='over'] { 
background-image:url(images/v2/EmailShare_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7emailshare[state='down'] { 
background-image:url(images/v2/EmailShare_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7emailshare[state='disabled'] { 
background-image:url(images/v2/EmailShare_dark_disabled.png); 
}
```

使用下列CSS類別選取器來控制對話方塊作用中時涵蓋網頁的背景覆蓋：

```
.s7ecatalogsearchviewer .s7emaildialog .s7backoverlay
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
.s7ecatalogsearchviewer .s7emaildialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

依預設，強制回應對話方塊會顯示在案頭系統的畫面中央，並取用觸控裝置上的整個網頁區域。 在所有情況下，對話框的定位和大小由元件管理。 對話方塊由下列CSS類別選取器控制：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialog
```

**對話框的CSS屬性**

<table id="table_5272BC8EF9124018B4290356B95B5559"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊框半徑  </span> </p> </td> 
   <td colname="col2"> <p> 對話框邊框半徑（如果對話框未佔據整個瀏覽器窗口）; </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景顏色  </span> </p> </td> 
   <td colname="col2"> <p> 對話框背景顏色； </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度  </span> </p> </td> 
   <td colname="col2"> <p> 應未設定或設為100%，在此情況下，對話方塊會進入整個瀏覽器視窗（觸控裝置最好使用此模式）; </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度  </span> </p> </td> 
   <td colname="col2"> <p> 應未設定或設為100%，在此情況下，對話方塊會進入整個瀏覽器視窗（觸控裝置最好使用此模式）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例：若要設定對話方塊以使用整個瀏覽器視窗，且在觸控裝置上具有白色背景：

```
.s7ecatalogsearchviewer .s7touchinput .s7emaildialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

對話框標題由表徵圖、標題文本和關閉按鈕組成。 標題容器可透過下列CSS類別選取器控制

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheader
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

圖示和標題文字會包裝在另一個由

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheader .s7dialogline
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
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheadericon
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
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheadertext
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
.s7ecatalogsearchviewer .s7emaildialog .s7closebutton
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

範例 — 若要設定對話方塊標題，使用邊框間距、24 x 17像素圖示、粗體16點標題和28 x 28像素「關閉」按鈕，該按鈕從上方放置兩個像素，從對話方塊容器的右側放置兩個像素：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheader { 
 padding: 10px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgemail_cap.png"); 
    height: 17px; 
    width: 24px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

對話框頁尾由取消和發送電子郵件按鈕組成。 頁尾容器可透過下列CSS類別選取器控制：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogfooter
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

頁尾具有保持兩個按鈕的內部容器。 它由下列CSS類別選取器控制：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbuttoncontainer
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
.s7ecatalogsearchviewer .s7emaildialog .s7dialogcancelbutton
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

使用下列CSS類選擇器控制「發送電子郵件」按鈕：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogactionbutton
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
.s7ecatalogsearchviewer .s7emaildialog .s7dialogfooter .s7button
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

此按鈕工具提示可本地化。 如需詳細資訊，請參閱[使用者介面元素本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 。

範例 — 若要設定對話方塊頁尾，其中包含64 x 34取消按鈕和82 x 34傳送電子郵件按鈕，且每個按鈕狀態的文字顏色和背景顏色會有所不同：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

主對話框區域（在頁首和頁尾之間）包含右側的可滾動對話框內容和滾動面板。 在所有情況下，元件會管理此區域的寬度，因此無法在CSS中設定它。 主對話框區域由以下CSS類選擇器控制：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogviewarea
```

**對話框查看區域的CSS屬性**

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度  </span> </p> </td> 
   <td colname="col2"> <p> 主對話框區域的高度。 只有在對話方塊以案頭模式運作時，才應指定它。 當對話方塊的大小為佔用整個瀏覽器視窗時，則不適用。 </p> </td> 
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

>[!NOTE]
>
>主對話框區域支援可選的`state`屬性選擇器。 提交電子郵件表單時，此欄位會設為`sendsuccess`，對話方塊會顯示確認訊息。 只要確認訊息很小，此屬性選取器就可用來在顯示此類確認訊息時降低對話方塊高度。

範例 — 若要在顯示確認訊息時將主對話方塊區域設定為300像素高度和100像素高度，請有10個像素邊界，然後使用白色背景：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogviewarea[state='sendsuccess'] { 
 height:100px; 
}
```

所有表單內容（如標籤和輸入欄位）都駐留在由以下CSS類選擇器控制的容器內：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody
```

如果此容器的高度似乎大於主對話框區域，則元件會自動啟用垂直捲動。

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
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody { 
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

對話框窗體中的所有靜態標籤都使用以下CSS類選擇器進行控制：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoglabel
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
.s7ecatalogsearchviewer .s7emaildialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

表單輸入欄位左側顯示的所有靜態標籤都以下列方式控制：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputlabel
```

**對話框輸入標籤的CSS屬性**

<table id="table_B5CF02837BAA42C7B79B6D9DA20792DF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度  </span> </p> </td> 
   <td colname="col2"> <p>靜態標籤的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 文本對齊  </span> </p> </td> 
   <td colname="col2"> <p>水準文本對齊方式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊際  </span> </p> </td> 
   <td colname="col2"> <p>靜態標籤邊界。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填補 </span> </p> </td> 
   <td colname="col2"> <p>靜態標籤填充。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例：若要將輸入欄位標籤設為50像素寬、對齊右、邊框間距為10像素，右側為10像素邊距：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputlabel { 
    margin-right: 10px; 
    padding: 10px; 
    text-align: right; 
    width: 50px; 
}
```

每個表單輸入欄位都會包裝在容器中，讓您在輸入欄位周圍套用自訂邊框。 它由下列CSS類別選取器控制：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputcontainer
```

**對話框輸入容器的CSS屬性**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊框  </span> </p> </td> 
   <td colname="col2"> <p>輸入欄位容器周圍的邊框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填補 </span> </p> </td> 
   <td colname="col2"> <p>內部填充。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>輸入欄位容器支援選用的`state`屬性選擇器。 當使用者在輸入資料格式中發生錯誤，且內嵌驗證失敗時，此值會設為`verifyerror`。 此屬性選擇器可用來反白標示表單中錯誤的使用者輸入。

從對話框主體的左至右邊緣（包括「從」欄位和「消息」欄位）的標籤擴散的大多數輸入欄位都通過以下CSS類選擇器進行控制：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputwide
```

**對話框輸入寬欄位的CSS屬性**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度  </span> </p> </td> 
   <td colname="col2"> <p>輸入欄位寬度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

「收件人」欄位較窄，因為它為右側的「刪除電子郵件」按鈕分配了空間。 它由下列CSS類別選取器控制：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputshort
```

**對話框輸入短欄位的CSS屬性**

<table id="table_DFA9059209FF4184BD483A529424E97F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度  </span> </p> </td> 
   <td colname="col2"> <p>輸入欄位寬度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例：設定表單，使表單有一個像素灰色邊框，在所有輸入欄位周圍有九個像素的邊框間距；若要對驗證失敗的欄位使用相同的紅色邊框，請為250像素寬的「收件人」欄位，其餘的輸入欄位為300像素寬：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 9px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputcontainer[state="verifyerror"] { 
    border: 1px solid #FF0000; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputshort { 
    width: 250px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputwide { 
    width: 300px; 
}
```

電子郵件輸入欄位另外受以下項目控制：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogmessage
```

此類允許您為基礎`TEXTAREA`元素設定特定屬性。

**對話框消息的CSS屬性**

<table id="table_9E9D5A0C3CDB45739615C4C07F8DC046"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度  </span> </p> </td> 
   <td colname="col2"> <p>訊息高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 繞字  </span> </p> </td> 
   <td colname="col2"> <p>文字繞排樣式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例：若要將電子郵件訊息設定為50像素高，並使用`break-word`文字繞排：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogmessage { 
    height: 50px; 
    word-wrap: break-word; 
}
```

「新增其他電子郵件地址」按鈕可讓使用者在電子郵件表單中新增多個地址。 它由下列CSS類別選取器控制：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogaddemailbutton
```

**對話框的CSS屬性添加電子郵件地址按鈕**

<table id="table_8829DC0694684E8BA427DFB821F7433D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度  </span> </p> </td> 
   <td colname="col2"> <p>按鈕高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 色彩  </span> </p> </td> 
   <td colname="col2"> <p>每個狀態的按鈕文字顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景 — 影像  </span> </p> </td> 
   <td colname="col2"> <p>每個狀態的按鈕影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p>按鈕區域內的按鈕影像位置。 </p> </td> 
  </tr> 
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
   <td colname="col2"> <p>按鈕內的文字高度。 影響垂直對齊。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 文本對齊  </span> </p> </td> 
   <td colname="col2"> <p>水準文字對齊。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填補 </span> </p> </td> 
   <td colname="col2"> <p>內部填充。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援`state`屬性選擇器，可用於將不同的外觀應用於不同的按鈕狀態。

按鈕工具提示可以本地化。 如需詳細資訊，請參閱[使用者介面元素本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 。

範例：若要將「新增其他電子郵件地址」按鈕設定為高25像素，請使用12點粗體字型並以右對齊，並針對每個狀態使用不同的文字顏色和影像：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogaddemailbutton { 
 text-align:right; 
 font-size:12pt; 
 font-weight:bold; 
 background-position:left center; 
 line-height:25px; 
 padding-left:30px; 
 height:25px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogaddemailbutton[state='up'] { 
 color:#666666; 
 background-image:url(images/sdk/dlgaddplus_up.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogaddemailbutton[state='down'] { 
 color:#000000; 
 background-image:url(images/sdk/dlgaddplus_over.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogaddemailbutton[state='over'] { 
 color:#000000; 
 text-decoration:underline; 
 background-image:url(images/sdk/dlgaddplus_over.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogaddemailbutton[state='disabled'] { 
 color:#666666; 
 background-image:url(images/sdk/dlgaddplus_up.png); 
}
```

「移除」按鈕可讓使用者從電子郵件表單中移除額外的地址。 它由下列CSS類別選取器控制：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogremoveemailbutton
```

**對話框的CSS屬性刪除電子郵件按鈕**

<table id="table_79E4C65741E64859B9C9E9DCCB3D050B"> 
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

按鈕工具提示可以本地化。 如需詳細資訊，請參閱[使用者介面元素本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 。

範例：若要將「移除」按鈕設定為25 x 25像素，並對每個狀態使用不同的影像：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogremoveemailbutton { 
 width:25px; 
 height:25px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogremoveemailbutton[state='up'] { 
 background-image:url(images/sdk/dlgremove_up.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogremoveemailbutton[state='over'] { 
 background-image:url(images/sdk/dlgremove_over.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogremoveemailbutton[state='down'] { 
 background-image:url(images/sdk/dlgremove_over.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogremoveemailbutton[state='disabled'] { 
 background-image:url(images/sdk/dlgremove_up.png); 
}
```

要共用的內容會顯示在對話方塊內文的底部，並包含縮圖、標題、來源URL和說明。 它會包裝在由下列CSS類別選取器控制的容器中：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogcontent
```

**對話框內容的CSS屬性**

<table id="table_9C5CBFC2482E4A46BE837573B0B02FE4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊框  </span> </p> </td> 
   <td colname="col2"> <p>容器邊框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填補 </span> </p> </td> 
   <td colname="col2"> <p>內部填充。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例：若要設定底部容器，使其具有一個像素點狀虛線邊框，且無邊框間距：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogcontent { 
    border: 1px dotted #A0A0A0; 
    padding: 0; 
}
```

縮圖影像是透過下列CSS類別選取器控制：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogthumbnail
```

`background-image`屬性由元件邏輯設定。

**對話框縮略圖影像的CSS屬性**

<table id="table_4C614FF2CEB149DAB5B7D7BC38CD3CAE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度  </span> </p> </td> 
   <td colname="col2"> <p>縮圖寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度  </span> </p> </td> 
   <td colname="col2"> <p>縮圖高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 垂直對齊  </span> </p> </td> 
   <td colname="col2"> <p>垂直對齊縮圖。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填補 </span> </p> </td> 
   <td colname="col2"> <p>內部填充。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例：若要將縮圖設為90 x 60像素，並以10個邊框對齊：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogthumbnail { 
    height: 60px; 
    padding: 10px; 
    vertical-align: top; 
    width: 90px; 
}
```

內容標題、來源和說明會進一步分組為內容縮圖右側的面板。 它由下列CSS類別選取器控制：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginfopanel
```

**對話框資訊面板的CSS屬性**

<table id="table_EDFA6229D8C3468E989E7EC05F23EF3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度  </span> </p> </td> 
   <td colname="col2"> <p>面板寬度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例：若要將內容資訊面板設定為300像素寬：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginfopanel { 
    width: 300px; 
}
```

使用下列CSS類別選取器控制內容標題：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogtitle
```

**對話框標題的CSS屬性**

<table id="table_E83C149E66EC474092DF8A180DA9A550"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊際  </span> </p> </td> 
   <td colname="col2"> <p>外邊距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型粗細  </span> </p> </td> 
   <td colname="col2"> <p>字型寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型大小  </span> </p> </td> 
   <td colname="col2"> <p>字型大小. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型系列  </span> </p> </td> 
   <td colname="col2"> <p>字型系列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例：若要設定內容標題以使用粗體字型，且有10個像素邊界：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogtitle { 
    font-weight: bold; 
    margin: 10px; 
}
```

使用下列CSS類別選取器控制內容來源：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogorigin
```

**對話框內容源的CSS屬性**

<table id="table_51763B532A9C4AE8AE54B69933A8C0B5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊際  </span> </p> </td> 
   <td colname="col2"> <p>外邊距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型粗細  </span> </p> </td> 
   <td colname="col2"> <p>字型寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型大小  </span> </p> </td> 
   <td colname="col2"> <p>字型大小. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型系列  </span> </p> </td> 
   <td colname="col2"> <p>字型系列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例：若要設定內容來源有10個像素邊界：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogorigin { 
    margin: 10px; 
}
```

使用下列CSS類選擇器控制內容說明：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogdescription
```

**對話框內容說明的CSS屬性**

<table id="table_F0F917ED3D1D4FCE974F48214D287E14"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊際  </span> </p> </td> 
   <td colname="col2"> <p>外邊距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型粗細  </span> </p> </td> 
   <td colname="col2"> <p>字型寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型大小  </span> </p> </td> 
   <td colname="col2"> <p>字型大小. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型系列  </span> </p> </td> 
   <td colname="col2"> <p>字型系列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例：若要設定內容說明，使其有10個像素邊界，並使用9個點字型：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogdescription { 
    font-size: 9pt; 
    margin: 10px; 
}
```

當使用者輸入錯誤的輸入資料且內嵌驗證失敗，或當提交表單時對話方塊需要呈現錯誤或確認訊息時，對話方塊內文頂端會顯示訊息。 它由下列CSS類別選取器控制：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogerrormessage
```

**對話框的CSS屬性錯誤消息**

<table id="table_C114E1004C334D339C25A3438E8E6614"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景 — 影像  </span> </p> </td> 
   <td colname="col2"> <p> 錯誤圖示。 預設為驚嘆號。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 訊息區域內的錯誤圖示位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 色彩  </span> </p> </td> 
   <td colname="col2"> <p>消息文本顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型粗細  </span> </p> </td> 
   <td colname="col2"> <p>字型寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型大小  </span> </p> </td> 
   <td colname="col2"> <p>字型大小. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型系列  </span> </p> </td> 
   <td colname="col2"> <p>字型系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 線高  </span> </p> </td> 
   <td colname="col2"> <p> 訊息內的文字高度。 影響垂直對齊。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填補 </span> </p> </td> 
   <td colname="col2"> <p>內部填充。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此消息支援`state`屬性選擇器，其可能值如下：`verifyerror`、`senderror`和`sendsuccess`。 `verifyerror` 在因內嵌輸入驗證失敗而顯示訊息時設定； `senderror` 是在後端電子郵件服務回報錯誤時設定； `sendsuccess` 在成功傳送電子郵件時設定。這樣，根據對話框狀態，可以以不同方式設定消息的樣式。

按鈕工具提示可以本地化。 如需詳細資訊，請參閱[使用者介面元素本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 。

範例：若要設定訊息，使用十點粗體字型、25像素行高、左側邊框20像素邊框間距、使用驚嘆號圖示、發生錯誤時使用紅色文字、成功時沒有圖示和綠色文字：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogerrormessage[state="verifyerror"] { 
    background-image: url("images/sdk/dlgerrimg.png"); 
    color: #FF0000; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogerrormessage[state="senderror"] { 
    background-image: url("images/sdk/dlgerrimg.png"); 
    color: #FF0000; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogerrormessage[state="sendsuccess"] { 
    background-image: none; 
    color: #00B200; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogerrormessage { 
    background-position: left center; 
    font-size: 10pt; 
    font-weight: bold; 
    line-height: 25px; 
    padding-left: 20px; 
}
```

如果需要垂直捲動，則會在對話方塊右邊緣附近的面板中呈現捲軸，該對話方塊由下列CSS類別選取器控制：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogscrollpanel
```

**對話框滾動面板的CSS屬性**

<table id="table_A0C3AC7E00544FFBB8E1364F4CDDB371"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度  </span> </p> </td> 
   <td colname="col2"> <p>捲動面板寬度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例：若要將捲動面板設定為44像素寬：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogscrollpanel { 
    width: 44px; 
}
```

使用以下CSS類選擇器控制捲動條區域的外觀：

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar
```

**捲軸的CSS屬性**

<table id="table_2BF74CF43E9B42D79F99A3F5208D7051"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度  </span> </p> </td> 
   <td colname="col2"> <p> 捲軸寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 頂部 </span> </p> </td> 
   <td colname="col2"> <p> 垂直捲動條從捲動面板的頂部偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p> 垂直捲動條從捲動面板底部偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右側 </span> </p> </td> 
   <td colname="col2"> <p> 水準捲動條從捲動面板的右邊緣偏移。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要設定寬28像素的捲軸，從捲軸面板的上、右、下各8像素的邊界：

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar { 
    bottom: 8px; 
    right: 8px; 
    top: 8px; 
    width: 28px; 
}
```

捲動條軌跡是頂部和底部捲動按鈕之間的區域。 元件會自動設定軌跡的位置和高度。 使用下列CSS類別選取器控制追蹤：

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolltrack
```

**捲動追蹤的CSS屬性**

<table id="table_EE990E7A342843619EDD84BAD29C6F2A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度  </span> </p> </td> 
   <td colname="col2"> <p>軌道寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景顏色  </span> </p> </td> 
   <td colname="col2"> <p>追蹤背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例：若要設定寬28像素且背景灰色的捲軸軌道：

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolltrack { 
width:28px; 
background-color: #B2B2B2; 
}
```

捲動條縮圖在捲動軌道區域內垂直移動。 其垂直位置完全由元件邏輯控制，但縮圖高度不會根據內容量而動態改變。 您可以使用下列CSS類別選取器來設定縮圖高度和其他方面：

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollthumb
```

**捲動條縮圖的CSS屬性**

<table id="table_5A4A283A50044A51881D997885674BDF"> 
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
   <td colname="col1"> <p> <span class="codeph"> 邊框間距 — 頂端  </span> </p> </td> 
   <td colname="col2"> <p> 軌道頂端之間的垂直邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊框間距  </span> </p> </td> 
   <td colname="col2"> <p> 軌道底部之間的垂直邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景 — 影像  </span> </p> </td> 
   <td colname="col2"> <p>為給定拇指狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS精靈，則位於圖稿精靈內。 </p> <p>另請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Thumb支援`state`屬性選擇器，可用於將不同外觀應用於不同的Thumb狀態：`up`、`down`、`over`和`disabled`。

示例 — 要設定捲動條縮圖，該縮圖為28 x 45像素，在頂部和底部有10個像素邊距，並且每個狀態的圖稿都不同：

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollthumb { 
    height: 45px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 28px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="up"] { 
 background-image:url("images/sdk/scrollbar_thumb_up.png"); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="down"] { 
 background-image:url("images/sdk/scrollbar_thumb_down.png"); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="over"] { 
 background-image:url("images/sdk/scrollbar_thumb_over.png"); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="disabled"] { 
 background-image:url("images/sdk/scrollbar_thumb_disabled.png"); 
}
```

使用以下CSS類選擇器控制頂部和底部捲動按鈕的外觀：

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollupbutton
```

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton
```

無法使用CSS `top`、`left`、`bottom`和`right`屬性來定位捲動按鈕。 反之，檢視器邏輯會自動定位。

**頂部和底部捲動按鈕的CSS屬性**

<table id="table_EB853317E08941979B0E141C3C9B2C49"> 
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
   <td colname="col1"> <p> <span class="codeph"> 背景 — 影像  </span> </p> </td> 
   <td colname="col2"> <p>針對指定按鈕狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS精靈，則位於圖稿精靈內。 </p> <p>另請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>這些按鈕支援`state`屬性選擇器，可用於將不同的外觀應用於不同的按鈕狀態：`up`、`down`、`over`和`disabled`。

按鈕工具提示可以本地化。 如需詳細資訊，請參閱[使用者介面元素本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 。

示例 — 要設定28 x 32像素的捲動按鈕，並且每個狀態的圖稿不同：

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='up'] { 
background-image:url(images/sdk/scroll_up_up.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/scroll_up_over.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/scroll_up_down.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_up_disabled.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/scroll_down_up.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/scroll_down_over.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/scroll_down_down.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_down_disabled.png); 
}
```
