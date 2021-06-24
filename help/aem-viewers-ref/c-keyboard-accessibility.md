---
description: 基本縮放、eCatalog、eCatalog搜尋、彈出、內嵌縮放、混合媒體、回轉、視訊、縮放、維度(3D)、轉盤、互動式影像、互動式視訊和Video360檢視器介面中公開的所有功能都可透過鍵盤存取。
solution: Experience Manager
title: 鍵盤協助工具和導覽
feature: Dynamic Media Classic，檢視器，SDK/API
role: Developer,Business Practitioner
exl-id: 0bdf172a-0bde-42d2-900f-f207538fe588
source-git-commit: 62234233bb1a5bcbd0eac5d281b42ed785c0c169
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 0%

---

# 鍵盤協助工具和導覽{#keyboard-accessibility-and-navigation}

基本縮放、eCatalog、eCatalog搜尋、彈出、內嵌縮放、混合媒體、回轉、視訊、縮放、輪播、維度(3D)、互動式影像、互動式視訊和Video360檢視器介面中公開的所有功能都可透過鍵盤存取。

<!-- Updated June 1, 2020 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## 鍵盤協助工具和導覽 {#topic-f5650e9493404e55a3627c8d1366b861}

基本縮放、eCatalog、eCatalog搜尋、彈出、內嵌縮放、混合媒體、回轉、視訊、縮放、輪播、維度(3D)、互動式影像、互動式視訊和Video360檢視器介面中公開的所有功能都可透過鍵盤存取。

最終用戶可使用&#x200B;**[!UICONTROL Tab]**&#x200B;和&#x200B;**[!UICONTROL Shift+Tab]**&#x200B;鍵擊在查看器用戶介面元素之間導航。 使用&#x200B;**[!UICONTROL Tab]**&#x200B;將輸入焦點按Tab鍵順序提前到下一個用戶介面元素；使用&#x200B;**[!UICONTROL Shift+Tab]**&#x200B;將輸入焦點調回上一個使用者介面元素。 焦點周遊會遵循畫面上的自然使用者介面元素位置，並依從左至右、由上至下的順序移動。

根據作業系統和Web瀏覽器設定，具有輸入焦點的用戶介面元素接收視覺焦點指示。 例如，視覺指示器可以是圍繞用戶介面元素呈現的細邊框。

您可以在檢視器CSS中停用或自訂此類焦點醒目提示。 在此幫助系統的目錄中，在特定的查看器名稱（例如，基本縮放或交互視頻）下，按一下「自定義&#x200B;*查看器***&#x200B;名稱> **焦點突出顯示**」。**

多數情況下，由單個查看器用戶介面元素支援的擊鍵是顯而易見的，並且易於發現。

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
   <td colname="col2"> <p>空格或Enter鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>放大或縮小 </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol"> + </span> 或 <span class="uicontrol"> -  </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>縮放重設 </p> </td> 
   <td colname="col2"> <p>Esc鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>平移 </p> </td> 
   <td colname="col2"> <p>向上、向下、向左或向右鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>旋轉360度的影像 </p> </td> 
   <td colname="col2"> <p>影像處於重設狀態時，請使用方向鍵。 </p> <p>使用多維回轉集時，請使用向上或向下鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>產品色票選擇 </p> </td> 
   <td colname="col2"> <p>上、下、左、右箭頭鍵；首頁或結束金鑰。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>產品色票啟動 </p> </td> 
   <td colname="col2"> <p>空格或Enter鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>視訊和互動式視訊，逐步倒帶 </p> </td> 
   <td colname="col2"> <p>向左或向上鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>視訊和互動式視訊，快進 </p> </td> 
   <td colname="col2"> <p>向右或向下箭頭鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>視訊和互動式視訊，前往開始或結束 </p> </td> 
   <td colname="col2"> <p>Home或End金鑰。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>視訊和互動式視訊，當焦點在滑桿上時可控制音量等級 </p> </td> 
   <td colname="col2"> <p>上、下、左、右箭頭鍵；首頁或結束金鑰。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>視訊和互動式視訊，可變音量 </p> </td> 
   <td colname="col2"> <p>當焦點位於其滑塊部分時，用於控制音量級別的箭頭、首頁和結束鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>視訊，當顯示強制回應對話方塊時，焦點周遊會限制為僅限對話方塊控制項。 </p> </td> 
   <td colname="col2"> <p>按Esc鍵關閉對話框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>輪播，在主檢視中變更橫幅影像 </p> </td> 
   <td colname="col2"> <p>向左或向右鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>輪播、熱點選取和熱點啟動 </p> </td> 
   <td colname="col2"> <p>熱點選擇：上、下、左或右箭頭鍵 </p> <p>熱點激活：空格或Enter鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog，在主檢視中變更頁面影像 </p> </td> 
   <td colname="col2"> <p> 向左或向右方向鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog，縮圖選取 </p> </td> 
   <td colname="col2"> <p>方向鍵；Home和End密鑰。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog，色票啟動 </p> </td> 
   <td colname="col2"> <p>空格或Enter鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog，熱點選擇 </p> </td> 
   <td colname="col2"> <p>方向鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog，啟動 </p> </td> 
   <td colname="col2"> <p>空格或輸入鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog，啟用下拉式元件 </p> </td> 
   <td colname="col2"> <p> 向下鍵；空格或Enter鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog，何時焦點置於下拉式清單中 </p> </td> 
   <td colname="col2"> <p>在啟動面板之前，使用方向鍵選取面板中的特定項目。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog中，當顯示強制回應對話方塊時，焦點周遊會限制為僅限對話方塊控制項。 </p> </td> 
   <td colname="col2"> <p>按Esc鍵關閉對話框。 </p> </td> 
  </tr> 
 </tbody> 
</table>
