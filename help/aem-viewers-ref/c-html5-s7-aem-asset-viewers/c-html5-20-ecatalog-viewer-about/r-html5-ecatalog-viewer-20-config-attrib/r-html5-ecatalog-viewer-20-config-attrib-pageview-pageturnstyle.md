---
title: PageView.pageturnstyle
description: PageView.pageturnstyle
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 00706c64-c051-4b62-8194-61d0a1c565e9
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 3%

---

# PageView.pageturnstyle{#pageview-pageturnstyle}

` [PageView.|<containerId>_pageView.]pageturnstyle= *`diferWidth`*, *`diferColor`*, *`diferOpacity`*, *`borderOnOff`*, *`borderColor`*, *`fillColor`*`

當 `PageView.frametransition` 設為 `turn` 或 `auto` 在案頭系統上。

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
   <td colname="col2"> <p>在 <span class="codeph"> 0</span> to <span class="codeph"> 1</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderOnOff</span></span> </p> </td> 
   <td colname="col2"> <p> 標幟( <span class="codeph"> 0</span> 或 <span class="codeph"> 1</span>)，可開啟或關閉開啟的頁面周圍的邊框。 </p> </td> 
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

`40,909090,1,1,909090,FFFFFF`

## 範例 {#section-bb97b2aac37a43eba11d263ce7049363}

`pageturnstyle=20,FF0000,1,1,00FF00,0000FF`
