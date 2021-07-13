---
description: 連結分享工具包含新增至Social分享面板的按鈕，以及啟動工具時顯示的強制回應對話方塊。 按鈕的位置由Social分享工具完全管理。
solution: Experience Manager
title: 連結共用
feature: Dynamic Media Classic，檢視器，SDK/API,360 VR影片
role: Developer,User
exl-id: 9eb2ef38-9b86-4c60-90a2-6609cb3fcc39
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '1390'
ht-degree: 2%

---

# 連結共用{#link-share}

連結分享工具包含新增至Social分享面板的按鈕，以及啟動工具時顯示的強制回應對話方塊。 按鈕的位置由Social分享工具完全管理。

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

連結共用按鈕的外觀由下列CSS類別選取器控制：

```
.s7video360viewer .s7linkshare
```

**連結共用工具的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>按鈕寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>按鈕高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景 — 影像  </span> </p> </td> 
   <td colname="col2"> <p> 針對指定按鈕狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS精靈，則位於圖稿精靈內。 </p> <p>請參閱<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援`state`屬性選擇器，可用於將不同的外觀應用於不同的按鈕狀態。

您可以在其CSS類別上設定`display:none` CSS屬性，從Social共用面板中移除按鈕。

按鈕工具提示可以本地化。 請參閱[使用者介面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1)。

範例：若要設定28 x 28像素的連結共用按鈕，並針對四個不同按鈕狀態中的每一個顯示不同的影像：

```
.s7video360viewer .s7linkshare { 
 width:28px; 
 height:28px; 
} 
.s7video360viewer .s7linkshare[state='up'] { 
background-image:url(images/v2/LinkShare_dark_up.png); 
} 
.s7video360viewer .s7linkshare[state='over'] { 
background-image:url(images/v2/LinkShare_dark_over.png); 
} 
.s7video360viewer .s7linkshare[state='down'] { 
background-image:url(images/v2/LinkShare_dark_down.png); 
} 
.s7video360viewer .s7linkshare[state='disabled'] { 
background-image:url(images/v2/LinkShare_dark_disabled.png); 
}
```

當對話方塊處於作用中狀態時，會使用下列CSS類別選取器來控制覆蓋網頁的背景覆蓋：

```
.s7video360viewer .s7linkdialog .s7backoverlay
```

**背景覆蓋的CSS屬性**

<table id="table_DB4183CE8061425084D495A355A941F8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 不透明度  </span> </p> </td> 
   <td colname="col2"> <p>背景覆蓋圖不透明度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景顏色  </span> </p> </td> 
   <td colname="col2"> <p>背景覆蓋圖顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**範例**  — 若要設定背景覆蓋圖為灰色且不透明度為70%:

```
.s7video360viewer .s7linkdialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

依預設，強制回應對話方塊會顯示在案頭系統的畫面中央，並在觸控裝置上取用整個網頁區域。 在所有情況下，對話框的定位和大小由元件管理。 使用以下CSS類選擇器控制該對話框：

```
.s7video360viewer .s7linkdialog .s7dialog
```

**對話框的CSS屬性**

<table id="table_E31711ADF4C7446182549244362199A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊框半徑  </span> </p> </td> 
   <td colname="col2"> <p> 對話框邊框半徑，以防對話框不佔用整個瀏覽器。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景顏色  </span> </p> </td> 
   <td colname="col2"> <p>對話框背景顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度  </span> </p> </td> 
   <td colname="col2"> <p>應為未設定或設為100%，在此情況下，對話方塊會取用整個瀏覽器視窗（觸控裝置最好使用此模式）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度  </span> </p> </td> 
   <td colname="col2"> <p>應為未設定或設為100%，在此情況下，對話方塊會取用整個瀏覽器視窗（觸控裝置最好使用此模式）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**範例**  — 若要設定對話方塊以使用整個瀏覽器視窗，且在觸控裝置上具有白色背景：

```
.s7video360viewer.s7touchinput .s7linkdialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

對話框標題由表徵圖、標題文本和關閉按鈕組成。 標題容器可透過下列CSS類別選取器控制：

```
.s7video360viewer .s7linkdialog .s7dialogheader
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

圖示和標題文字會包裝在另一個由下列CSS類別選取器控制的容器中：

```
.s7video360viewer .s7linkdialog .s7dialogheader .s7dialogline
```

**對話框行的CSS屬性**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填補 </span> </p> </td> 
   <td colname="col2"> <p> 頁首圖示和標題的內邊框間距 </p> </td> 
  </tr> 
 </tbody> 
</table>

使用下列CSS類選擇器控制標題表徵圖

```
.s7video360viewer .s7linkdialog .s7dialogheadericon
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
   <td colname="col2"> <p> 如果使用CSS精靈，則位於圖稿精靈內。 </p> <p>請參閱<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

使用下列CSS類選擇器控制標題：

```
.s7video360viewer .s7linkdialog .s7dialogheadertext
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
.s7video360viewer .s7linkdialog .s7closebutton
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
   <td colname="col2"> <p> 如果使用CSS精靈，則位於圖稿精靈內。 </p> <p>請參閱<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援`state`屬性選擇器，可用於將不同的外觀應用於不同的按鈕狀態。

「關閉」按鈕工具提示和對話框標題可以本地化。 請參閱[使用者介面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1)。

**範例**  — 若要設定對話方塊標題，並加上邊框間距、22 x 12像素圖示、粗體16點標題和28 x 28像素關閉按鈕，此按鈕的位置為從上方兩個像素，以及從對話方塊容器右側兩個像素：

```
.s7video360viewer .s7linkdialog .s7dialogheader { 
 padding: 10px; 
} 
.s7video360viewer .s7linkdialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7video360viewer .s7linkdialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlglink_cap.png"); 
    height: 12px; 
    width: 22px; 
} 
.s7video360viewer .s7linkdialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7video360viewer .s7linkdialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7video360viewer .s7linkdialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7video360viewer .s7linkdialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7video360viewer .s7linkdialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7video360viewer .s7linkdialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

對話框頁尾由「取消」按鈕組成。 頁尾容器可透過下列CSS類別選取器控制：

```
.s7video360viewer .s7linkdialog .s7dialogfooter
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

頁尾具有保持按鈕的內部容器。 它由下列CSS類別選取器控制：

```
.s7video360viewer .s7linkdialog .s7dialogbuttoncontainer
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

使用以下CSS類選擇器控制「全部選擇」按鈕：

```
.s7video360viewer .s7linkdialog .s7dialogactionbutton
```

按鈕僅在案頭系統上可用。

**「全部選擇」按鈕的CSS屬性**

<table id="table_021D0467632F49FEBFDF4CF96D2D67C7"> 
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
>「全部選擇」按鈕支援`state`屬性選擇器，它可用於將不同的外觀應用於不同的按鈕狀態。

使用以下CSS類選擇器控制取消按鈕：

```
.s7video360viewer .s7linkdialog .s7dialogcancelbutton
```

**對話框的CSS屬性取消按鈕**

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
.s7video360viewer .s7linkdialog .s7dialogfooter .s7button
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

按鈕工具提示可翻譯。 請參閱[使用者介面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1)。

**範例**  — 若要使用64 x 34取消按鈕設定對話方塊頁尾，其文字顏色和背景顏色會因每個按鈕狀態而不同：

```
.s7video360viewer .s7linkdialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7video360viewer .s7linkdialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7video360viewer .s7linkdialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

主對話框區域（在頁首和頁尾之間）包含對話框內容。 在所有情況下，元件都會管理此區域的寬度 — 無法在CSS中設定它。 主對話框區域由以下CSS類選擇器控制：

```
.s7video360viewer .s7linkdialog .s7dialogviewarea
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

**範例**  — 若要將主對話方塊區域設定為300像素高、有10像素邊界，並使用白色背景：

```
.s7video360viewer .s7linkdialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
}
```

所有表單內容（例如標籤和輸入欄位）都駐留在由以下CSS類選擇器控制的容器內：

```
.s7video360viewer .s7linkdialog .s7dialogbody
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

**範例**  — 若要設定表單內容，應有10個像素邊框間距：

```
.s7interactivevideoviewer .s7linkdialog .s7dialogbody { 
    padding: 10px; 
}
```

對話框窗體中的所有靜態標籤都使用

```
.s7video360viewer .s7linkdialog .s7dialoglabel
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

對話方塊標籤可以翻譯。 請參閱[使用者介面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1)。

**範例**  — 若要將所有標籤設為灰色、粗體和九像素字型：

```
.s7video360viewer .s7linkdialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

使用下列CSS類別選取器來控制顯示在連結頂端的文字副本大小：

```
.s7video360viewer .s7linkdialog .s7dialoginputwide
```

**對話框輸入寬欄位的CSS屬性**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度  </span> </p> </td> 
   <td colname="col2"> <p>文字寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填補 </span> </p> </td> 
   <td colname="col2"> <p>內部填充。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**範例**  — 若要將文字復本設為430像素寬，且底部有10像素邊框：

```
.s7video360viewer .s7linkdialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

共用連結會包裝在容器中，並透過下列CSS類別選取器加以控制：

```
.s7video360viewer .s7linkdialog .s7dialoginputcontainer
```

**對話框輸入容器的CSS屬性**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊框  </span> </p> </td> 
   <td colname="col2"> <p>共用連結容器周圍的邊框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填補 </span> </p> </td> 
   <td colname="col2"> <p>內部填充。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**範例**  — 若要在內嵌程式碼文字周圍設定一個像素灰色邊框，並有九個像素的邊框間距：

```
.s7video360viewer .s7linkdialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 9px; 
}
```

共用連結本身由下列CSS類別選取器控制：

```
.s7video360viewer .s7linkdialog .s7dialoglink
```

**對話框的CSS屬性共用連結**

<table id="table_65CF778F5BDA45118208538DCBE203FB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度  </span> </p> </td> 
   <td colname="col2"> <p>共用連結寬度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**範例**  — 若要將共用連結設為450像素寬：

```
.s7video360viewer .s7linkdialog .s7dialoglink { 
    width: 450px; 
}
```
