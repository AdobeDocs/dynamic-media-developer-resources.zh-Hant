---
title: 設定指示器
description: 設定指示器是在觸摸設備上使用查看器時在主色板上呈現的一系列點。 當滾動按鈕不可用時，這些點可幫助用戶瀏覽縮略圖頁面。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 53ee058a-cb8c-4b1f-bb9b-caaecc12c947
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 1%

---

# 設定指示器{#set-indicator}

設定指示器是在觸摸設備上使用查看器時在主色板上呈現的一系列點。 當滾動按鈕不可用時，這些點可幫助用戶瀏覽縮略圖頁面。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**設定指示器的CSS屬性**

使用以下CSS類選擇器控制設定指示器容器的外觀：

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
   <td colname="col1"> <p> <span class="codeph"> 背景色 </span> </p> </td> 
   <td colname="col2"> <p>設定指示器的十六進位格式的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要建立帶白色背景的集指示符：

```
.s7mixedmediaviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

使用CSS類選擇器控制單個設定指示器點的外觀：

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
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>設定指示器點的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>設定指示器點的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左邊距 </span> </p> </td> 
   <td colname="col2"> <p>左邊距（像素）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 上邊距 </span> </p> </td> 
   <td colname="col2"> <p>上邊距（像素）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊距右 </span> </p> </td> 
   <td colname="col2"> <p>右邊距（像素）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊距底 </span> </p> </td> 
   <td colname="col2"> <p>底邊距（像素）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊界半徑 </span> </p> </td> 
   <td colname="col2"> <p>邊框半徑（以像素為單位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景色 </span> </p> </td> 
   <td colname="col2"> <p>十六進位格式的背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>設定指示器點支援 `state` 屬性選擇器，可用於將不同外觀應用於不同的縮略圖狀態。 特別是， `state="selected"` 與縮略圖的當前頁面相對應， `state="unselected"` 與預設點狀態相對應。

示例 — 要建立一個15 x 15像素的設定指示器點，其中有兩個像素水準邊距、五個像素頂邊距、一個像素底邊距、12像素半徑、#D5D3D3預設顏色和#939393動顏色：

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
