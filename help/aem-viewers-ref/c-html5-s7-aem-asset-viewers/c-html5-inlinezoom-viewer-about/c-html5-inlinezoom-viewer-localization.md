---
title: 使用者介面元素的本地化
description: Flyout Viewer顯示的某些內容可能會經過本地化。 此內容包含使用者介面元素工具提示，以及在載入時由彈出式縮放檢視顯示的資訊訊息。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 49795aa1-07c7-4f2e-bfd9-51d6581898ed
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---

# 使用者介面元素的本地化{#localization-of-user-interface-elements}

Flyout Viewer顯示的某些內容可能會經過本地化。 此內容包含使用者介面元素工具提示，以及在載入時由彈出式縮放檢視顯示的資訊訊息。

檢視器中可本地化的每個文字內容，都會以名為SYMBOL的特殊檢視器SDK識別碼表示。 任何SYMBOL都有隨現成可用的檢視器提供的英文語言環境(`"en"`)的預設相關文字值，而且也可以視需要為許多語言環境設定使用者定義的值。

當檢視器啟動時，它會檢查目前的地區設定，檢視此類地區設定的每個受支援SYMBOL是否有使用者定義的值。 如果有的話，它會使用使用者定義的值；否則，它會回覆成現成的預設文字。

使用者定義的本地化資料可作為本地化JSON物件傳遞至檢視器。 此類物件包含支援的語言環境清單、每個語言環境的SYMBOL文字值，以及預設語言環境。

以下是這類本地化物件的範例：

```
{ 
"en":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Mouse over to zoom", 
"FlyoutZoomView.TIP_BUBBLE_TAP":"Tap and hold to zoom" 
 }, 
 "fr":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Passez la souris sur pour zoomer", 
"FlyoutZoomView.TIP_BUBBLE_TAP":"Appuyez et maintenez pour agrandir" 
}, 
defaultLocale:"en" 
}
```

在上述範例中，本地化物件定義了兩個地區設定（`"en"`和`"fr"`），並為每個地區設定中的兩個使用者介面元素提供本地化。

網頁程式碼應將這類本地化物件傳遞至檢視器建構函式，做為設定物件之`localizedTexts`欄位的值。 替代選項是呼叫`setLocalizedTexts(localizationInfo)`方法來傳遞本地化物件。

支援下列SYMBOL：

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>符號 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p>頂層檢視器元素的ARIA標籤。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>主要檢視元件的ARIA角色說明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>鍵盤使用者的ARIA使用提示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_OVER </span> </p> </td> 
   <td colname="col2"> <p>案頭系統的資訊訊息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_TAP </span> </p> </td> 
   <td colname="col2"> <p>觸控裝置的資訊訊息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>向左捲動按鈕的工具提示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>向右捲動按鈕的工具提示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>向上捲動按鈕的工具提示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>向下捲動按鈕的工具提示。 </p> </td> 
  </tr> 
 </tbody> 
</table>
