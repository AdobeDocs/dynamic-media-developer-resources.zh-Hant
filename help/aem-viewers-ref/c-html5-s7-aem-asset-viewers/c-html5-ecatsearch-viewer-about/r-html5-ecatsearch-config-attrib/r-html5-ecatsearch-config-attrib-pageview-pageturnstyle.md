---
description: PageView.pageturnstyle
solution: Experience Manager
title: PageView.pageturnstyle
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog搜尋
role: Developer,User
exl-id: 2669c8e2-c942-420f-8262-9d76d5c499a2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---

# PageView.pageturnstyle{#pageview-pageturnstyle}

[!DNL `[PageView.|<containerId>_pageView.]pageturnstyle= *``*, *``*, *``*, *``*, *``*, *`difiderWidthdiferColordiferOpacityborderOnOffborderColorfillColor`*`]

在案頭系統上將[!DNL `PageView.frametransition`]設定為[!DNL `turn`]或[!DNL `auto`]時控制元件外觀。

<table id="table_A8CDA1AE2680402A99BCD5DD371B225F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> diferWidth</span></span> </p> </td> 
   <td colname="col2"> <p> 分頁線陰影的寬度（像素），它分隔跨頁中的左頁和右頁。 它還控制車削頁面旁邊顯示的正在運行的陰影的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> diferOpacity</span></span> </p> </td> 
   <td colname="col2"> <p> RRGGBB格式的陰影顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> diferOpacity</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 0</span>到<span class="codeph"> 1</span>範圍內的陰影不透明度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderOnOff</span></span> </p> </td> 
   <td colname="col2"> <p> 標幟（<span class="codeph"> 0</span>或<span class="codeph"> 1</span>）可開啟或關閉開啟的頁面周圍的邊框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderColor</span></span> </p> </td> 
   <td colname="col2"> <p> RRGGBB格式的邊框顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> fillColor</span></span> </p> </td> 
   <td colname="col2"> <p> 在翻頁動畫期間使用的元件區域的實體填充的顏色，為RRGGBB格式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-54c634116cfe4f17813318e07539264c}

選填。

## 預設 {#section-43fd13f639c2480c82658fafeeaf0846}

[!DNL `40,909090,1,1,909090,FFFFFF`]

## 範例 {#section-bb97b2aac37a43eba11d263ce7049363}

[!DNL `pageturnstyle=20,FF0000,1,1,00FF00,0000FF`]
