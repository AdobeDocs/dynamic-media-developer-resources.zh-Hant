---
description: 基本縮放、eCatalog、eCatalog搜尋、彈出、內嵌縮放、混合媒體、回轉、視訊、縮放、尺寸(3D)、轉盤、互動式影像、互動式視訊和Video360檢視器介面中公開的所有功能都可透過鍵盤存取。
solution: Experience Manager
title: 鍵盤協助功能與導覽
feature: Dynamic Media經典，檢視器，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 8207cba7e75c6bff878ef7f11f74b19bb88f1d61
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# 鍵盤協助功能與導覽{#keyboard-accessibility-and-navigation}

基本縮放、eCatalog、eCatalog搜尋、彈出、內嵌縮放、混合媒體、回轉、視訊、縮放、轉盤、立體(3D)、互動式影像、互動式視訊和Video360檢視器介面中公開的所有功能都可透過鍵盤存取。

<!-- Updated June 1, 2020 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## 鍵盤協助功能與導覽{#topic-f5650e9493404e55a3627c8d1366b861}

基本縮放、eCatalog、eCatalog搜尋、彈出、內嵌縮放、混合媒體、回轉、視訊、縮放、轉盤、立體(3D)、互動式影像、互動式視訊和Video360檢視器介面中公開的所有功能都可透過鍵盤存取。

最終用戶可以使用&#x200B;**[!UICONTROL Tab]**&#x200B;和&#x200B;**[!UICONTROL Shift+Tab]**&#x200B;鍵擊在查看器用戶介面元素之間導航。 使用&#x200B;**[!UICONTROL Tab]**&#x200B;將輸入焦點提前到Tab鍵順序中的下一個用戶介面元素；使用&#x200B;**[!UICONTROL Shift+Tab]**&#x200B;將輸入焦點帶回先前的使用者介面元素。 焦點遍歷會遵循畫面上自然的使用者介面元素位置，並依從左至右、從上至下的順序移動。

根據作業系統和網頁瀏覽器設定，具有輸入焦點的用戶介面元素接收視覺焦點指示。 例如，視覺指示器可以是圍繞用戶介面元素呈現的細邊框。

您可以在檢視器CSS中停用或自訂此類焦點反白顯示。 在本說明系統的目錄中，在特定檢視器名稱（例如，基本縮放或互動式視訊）下，按一下「自訂檢視器&#x200B;***名稱*> > **焦點反白顯示**」。**

個別檢視器使用者介面元素支援的按鍵動作，在大多數情況下都十分明顯，而且易於發現。

<table id="table_8C49100412224324BF1DBF7FDFDCCBF8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>動作 </p> </th> 
   <th colname="col2" class="entry"> <p>擊鍵 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>啟動按鈕元件 </p> </td> 
   <td colname="col2"> <p>空格鍵或Enter鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>放大或縮小 </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol"> + </span> 或 <span class="uicontrol"> - </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>縮放重設 </p> </td> 
   <td colname="col2"> <p>Esc鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>平移 </p> </td> 
   <td colname="col2"> <p>向上、向下、向左或向右箭頭鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>旋轉360度影像 </p> </td> 
   <td colname="col2"> <p>當影像處於重設狀態時，請使用方向鍵。 </p> <p>使用多維回轉集時，請使用向上或向下鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>產品色票選擇 </p> </td> 
   <td colname="col2"> <p>向上、向下、向左或向右鍵；首頁或結束金鑰。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>產品色票啟動 </p> </td> 
   <td colname="col2"> <p>空格鍵或Enter鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>視訊和互動式視訊，漸進倒轉 </p> </td> 
   <td colname="col2"> <p>向左或向上鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>視訊與互動式視訊，快速前進 </p> </td> 
   <td colname="col2"> <p>向右或向下鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>視訊和互動式視訊，請至開始或結束 </p> </td> 
   <td colname="col2"> <p>Home或End金鑰。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>視訊和互動式視訊，在焦點位於滑桿時控制音量 </p> </td> 
   <td colname="col2"> <p>向上、向下、向左或向右鍵；首頁或結束金鑰。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>視訊和互動式視訊，可變音量 </p> </td> 
   <td colname="col2"> <p>當焦點位於滑塊部分時，箭頭鍵、主鍵和端鍵可控制音量。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>視訊中，當顯示模式對話方塊時，焦點遍歷會限制為對話框控制項。 </p> </td> 
   <td colname="col2"> <p>Esc鍵關閉對話框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>轉盤，變更主檢視中的橫幅影像 </p> </td> 
   <td colname="col2"> <p>向左或向右箭頭鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>轉盤、熱點選擇和熱點激活 </p> </td> 
   <td colname="col2"> <p>熱點選擇：向上、向下、向左或向右鍵 </p> <p>熱點激活：空格鍵或Enter鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog，變更主檢視中的頁面影像 </p> </td> 
   <td colname="col2"> <p> 向左或向右箭頭鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog、縮圖選擇 </p> </td> 
   <td colname="col2"> <p>方向鍵；首頁和首頁密鑰。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog、色票啟動 </p> </td> 
   <td colname="col2"> <p>空格鍵或Enter鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog，熱點選擇 </p> </td> 
   <td colname="col2"> <p>方向鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog，啟動 </p> </td> 
   <td colname="col2"> <p>空格鍵或輸入鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog，啟用下拉式元件 </p> </td> 
   <td colname="col2"> <p> 向下鍵；空格鍵或Enter鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog，何時將焦點放在下拉式浸漬面板中 </p> </td> 
   <td colname="col2"> <p>在啟動面板之前，使用方向鍵來選取面板中的特定項目。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog，當顯示模式對話框時，焦點遍歷將僅限於對話框控制項。 </p> </td> 
   <td colname="col2"> <p>Esc鍵關閉對話框。 </p> </td> 
  </tr> 
 </tbody> 
</table>
