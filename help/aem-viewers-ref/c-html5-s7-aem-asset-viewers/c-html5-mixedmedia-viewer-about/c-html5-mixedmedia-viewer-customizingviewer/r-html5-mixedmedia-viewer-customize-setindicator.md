---
title: 設定指標
description: 設定指標是在觸控裝置上使用檢視器時，呈現在主要色票上方的一系列點。 無法使用捲動按鈕時，圓點可協助使用者瀏覽縮圖頁面。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 53ee058a-cb8c-4b1f-bb9b-caaecc12c947
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# 設定指標{#set-indicator}

設定指標是在觸控裝置上使用檢視器時，呈現在主要色票上方的一系列點。 無法使用捲動按鈕時，圓點可協助使用者瀏覽縮圖頁面。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

設定指示器的&#x200B;**CSS屬性**

設定指標容器的外觀是由下列CSS類別選取器所控制：

```
.s7mixedmediaviewer .s7setindicator
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
   <td colname="col2"> <p>設定指示器的十六進位格式的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要建立具有白色背景的設定指示器：

```
.s7mixedmediaviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

個別設定指標點的外觀是由CSS類別選取器所控制：

`.s7mixedmediaviewer .s7setindicator .s7dot`

<table id="table_09B6E232FB94417392D101A7A653BE54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">寬度</span> </p> </td> 
   <td colname="col2"> <p>設定指標點的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>設定指標點的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">左邊界</span> </p> </td> 
   <td colname="col2"> <p>左邊界（畫素）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">上邊界</span> </p> </td> 
   <td colname="col2"> <p>上邊界（畫素）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">右邊界</span> </p> </td> 
   <td colname="col2"> <p>以畫素為單位的右邊界。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">邊緣底部</span> </p> </td> 
   <td colname="col2"> <p>下方邊界（畫素）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">邊框半徑</span> </p> </td> 
   <td colname="col2"> <p>邊框半徑（畫素）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色彩</span> </p> </td> 
   <td colname="col2"> <p>以十六進位格式表示的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>設定指標點支援`state`屬性選取器，可用來將不同的外觀元素套用至不同的縮圖狀態。 特別是，`state="selected"`對應於目前的縮圖頁面，`state="unselected"`對應於預設點狀態。

範例 — 若要建立一個15 x 15畫素的設定指標點，其水準邊界為2畫素，上邊界為5畫素，下邊界為1畫素，半徑為12畫素，預設顏色為#D5D3D3色，作用中顏色為#939393色：

```
.s7mixedmediaviewer .s7setindicator .s7dot { 
 width:15px; 
 height:15px; 
 margin-left:2px; 
 margin-top:5px; 
 margin-right:2px; 
 margin-bottom:1px; 
 border-radius:12px; 
 background-color:#D5D3D3;  
} 
.s7mixedmediaviewer .s7setindicator .s7dot[state="selected"] { 
 background-color:#939393;  
}
```
