---
title: 鍵盤輔助功能和導航
description: 基本縮放、eCatalog、eCatalog Search、Flyout、Inline Zoom、混合媒體、旋轉、視頻、縮放、維(3D)、旋轉軸、互動式影像、互動式視頻和Video360查看器介面中顯示的所有功能均可使用鍵盤。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 0bdf172a-0bde-42d2-900f-f207538fe588
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 0%

---

# 鍵盤輔助功能和導航{#keyboard-accessibility-and-navigation}

基本縮放、eCatalog、eCatalog Search、Flyout、Inline Zoom、混合媒體、旋轉、視頻、縮放、旋轉、尺寸(3D)、互動式影像、互動式視頻和Video360查看器介面中顯示的所有功能均可使用鍵盤。

<!-- Updated June 1, 2020 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## 鍵盤輔助功能和導航 {#topic-f5650e9493404e55a3627c8d1366b861}

基本縮放、eCatalog、eCatalog Search、Flyout、Inline Zoom、混合媒體、旋轉、視頻、縮放、旋轉、尺寸(3D)、互動式影像、互動式視頻和Video360查看器介面中顯示的所有功能均可使用鍵盤。

最終用戶可以使用 **[!UICONTROL 頁籤]** 和 **[!UICONTROL Shift+Tab鍵]** 擊鍵。 使用 **[!UICONTROL 頁籤]** 將輸入焦點提前到下一個用戶介面元素的Tabbing順序；使用 **[!UICONTROL Shift+Tab鍵]** 將輸入焦點返回到上一個用戶介面元素。 焦點遍歷遵循螢幕上的自然用戶介面元素位置，然後按從左到右、從上到下的順序移動。

根據作業系統和web瀏覽器設定，具有輸入焦點的用戶介面元素接收可視焦點指示。 例如，可視指示器可以是圍繞用戶介面元素呈現的細邊框。

可以在查看器CSS中禁用或自定義此類焦點突出顯示。 在此幫助系統的目錄中，在特定查看器名稱下（例如，「基本縮放」或「互動式視頻」），按一下 **自定義 *查看器名稱*** >**&#x200B;聚焦突出顯示&#x200B;**。

單個查看器用戶介面元素支援的擊鍵在大多數情況下是顯而易見的，並且易於發現。

<table id="table_8C49100412224324BF1DBF7FDFDCCBF8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>動作 </p> </th> 
   <th colname="col2" class="entry"> <p>擊鍵 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>激活按鈕元件 </p> </td> 
   <td colname="col2"> <p>空格鍵或Enter鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>放大或縮小 </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol"> + </span> 或 <span class="uicontrol"> - </span>的下界。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>縮放重置 </p> </td> 
   <td colname="col2"> <p>Esc鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>平移 </p> </td> 
   <td colname="col2"> <p>上、下、左或右箭頭鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>旋轉360度影像 </p> </td> 
   <td colname="col2"> <p>當影像處於重置狀態時使用箭頭鍵。 </p> <p>使用多維旋轉集時使用上箭頭或下箭頭鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>產品色板選擇 </p> </td> 
   <td colname="col2"> <p>上、下、左或右箭頭鍵；Home或End鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>產品色板激活 </p> </td> 
   <td colname="col2"> <p>空格鍵或Enter鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>視頻和互動式視頻，漸進倒帶 </p> </td> 
   <td colname="col2"> <p>左箭頭鍵或上箭頭鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>視頻和互動式視頻，快進 </p> </td> 
   <td colname="col2"> <p>向右或向下箭頭鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>視頻和互動式視頻，轉到開頭或結尾 </p> </td> 
   <td colname="col2"> <p>Home或End鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>視頻和互動式視頻，當焦點位於滑塊上時控制音量 </p> </td> 
   <td colname="col2"> <p>上、下、左或右箭頭鍵；Home或End鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>視頻和互動式視頻，可變卷 </p> </td> 
   <td colname="col2"> <p>箭頭、主鍵和結束鍵，以在焦點位於滑塊部分時控制音量。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>視頻，當顯示模式對話框時，焦點遍歷將僅限於對話框控制項。 </p> </td> 
   <td colname="col2"> <p>Esc鍵關閉對話框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>旋轉傳送，在主視圖中更改標題影像 </p> </td> 
   <td colname="col2"> <p>左或右箭頭鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>旋轉木馬、熱點選擇和熱點激活 </p> </td> 
   <td colname="col2"> <p>熱點選擇：上、下、左或右箭頭鍵 </p> <p>熱點激活：空格鍵或Enter鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>編錄，更改主視圖中的頁面影像 </p> </td> 
   <td colname="col2"> <p> 左箭頭鍵或右箭頭鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog，縮略圖選擇 </p> </td> 
   <td colname="col2"> <p>箭頭鍵；Home和End鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog，色板激活 </p> </td> 
   <td colname="col2"> <p>空格鍵或Enter鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog，熱點選擇 </p> </td> 
   <td colname="col2"> <p>箭頭鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog，激活 </p> </td> 
   <td colname="col2"> <p>空格鍵或Enter鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog，激活下拉元件 </p> </td> 
   <td colname="col2"> <p> 向下箭頭鍵；空格鍵或Enter鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog，當焦點在「拖放」面板中時 </p> </td> 
   <td colname="col2"> <p>在激活面板之前，使用箭頭鍵在面板中選擇特定項目。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>「目錄」(Catalog)，當顯示模式對話框時，焦點遍歷將僅限於對話框控制項。 </p> </td> 
   <td colname="col2"> <p>Esc鍵關閉對話框。 </p> </td> 
  </tr> 
 </tbody> 
</table>
