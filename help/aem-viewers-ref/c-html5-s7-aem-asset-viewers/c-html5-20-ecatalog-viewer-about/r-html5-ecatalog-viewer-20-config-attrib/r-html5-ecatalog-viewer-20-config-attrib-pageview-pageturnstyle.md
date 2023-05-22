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
ht-degree: 2%

---

# PageView.pageturnstyle{#pageview-pageturnstyle}

` [PageView.|<containerId>_pageView.]pageturnstyle= *`分隔線寬度`*, *`除法器顏色`*, *`除法器不透明度`*, *`邊框開啟關閉`*, *`邊框顏色`*, *`填充顏色`*`

在 `PageView.frametransition` 設定為 `turn` 或 `auto` 在台式機系統上。

<table id="table_A8CDA1AE2680402A99BCD5DD371B225F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 分隔線寬度</span></span> </p> </td> 
   <td colname="col2"> <p> 分頁陰影的寬度（以像素為單位），該陰影分隔跨頁中的左頁和右頁。 它還控制在車削頁面旁邊顯示的運行陰影的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 除法器不透明度</span></span> </p> </td> 
   <td colname="col2"> <p> RRGGBB格式的陰影顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 除法器不透明度</span></span> </p> </td> 
   <td colname="col2"> <p>範圍中的陰影不透明度 <span class="codeph"> 0</span> 至 <span class="codeph"> 1</span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 邊框開啟關閉</span></span> </p> </td> 
   <td colname="col2"> <p> 標誌( <span class="codeph"> 0</span> 或 <span class="codeph"> 1</span>)開啟和關閉關閉的邊框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 邊框顏色</span></span> </p> </td> 
   <td colname="col2"> <p> RRGGBB格式的邊框顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 填充顏色</span></span> </p> </td> 
   <td colname="col2"> <p> 在翻頁動畫期間使用的元件區域的實體填充的顏色，採用RRGGBB格式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-54c634116cfe4f17813318e07539264c}

選擇性.

## 預設 {#section-43fd13f639c2480c82658fafeeaf0846}

`40,909090,1,1,909090,FFFFFF`

## 範例 {#section-bb97b2aac37a43eba11d263ce7049363}

`pageturnstyle=20,FF0000,1,1,00FF00,0000FF`
