---
description: PageView.pageturnstyle
solution: Experience Manager
title: PageView.pageturnstyle
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 2669c8e2-c942-420f-8262-9d76d5c499a2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 2%

---

# PageView.pageturnstyle{#pageview-pageturnstyle}

[!DNL `[PageView.|<containerId>_pageView.]pageturnstyle= *`分隔線寬度`*, *`除法器顏色`*, *`除法器不透明度`*, *`邊框開啟關閉`*, *`邊框顏色`*, *`填充顏色`*`]

在 [!DNL `PageView.frametransition`] 設定為 [!DNL `turn`] 或 [!DNL `auto`] 在台式機系統上。

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

[!DNL `40,909090,1,1,909090,FFFFFF`]

## 範例 {#section-bb97b2aac37a43eba11d263ce7049363}

[!DNL `pageturnstyle=20,FF0000,1,1,00FF00,0000FF`]
