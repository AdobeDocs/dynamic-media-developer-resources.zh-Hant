---
description: Flyout檢視器顯示的某些內容可能會受到本地化的規範。 此內容包含使用者介面元素工具提示和資訊訊息，這些訊息會由載入時的彈出縮放檢視顯示。
seo-description: Flyout檢視器顯示的某些內容可能會受到本地化的規範。 此內容包含使用者介面元素工具提示和資訊訊息，這些訊息會由載入時的彈出縮放檢視顯示。
seo-title: 使用者介面元素的本地化
solution: Experience Manager
title: 使用者介面元素的本地化
topic: Dynamic media
uuid: efba09ad-200b-4540-8876-c9e462ec233a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 使用者介面元素的本地化{#localization-of-user-interface-elements}

Flyout檢視器顯示的某些內容可能會受到本地化的規範。 此內容包含使用者介面元素工具提示和資訊訊息，這些訊息會由載入時的彈出縮放檢視顯示。

檢視器中可本地化的每個文字內容，都會以稱為SYMBOL的特殊檢視器SDK識別碼來表示。 任何SYMBOL都有預設的英文地區設定( `"en"`)相關文字值，這是隨附於現成檢視器中。 此外，還可以視需要設定使用者定義的值。

當檢視器啟動時，會檢查目前的地區設定，以查看地區設定中每個支援的SYMBOL是否都有使用者定義的值。 若有，則使用使用者定義的值；否則，它會回到預設的預設文字。

使用者定義的本地化資料可以作為本地化JSON物件傳遞至檢視器。 此類對象包含支援的語言環境清單、每個語言環境的SYMBOL文本值以及預設語言環境。

此類本地化對象的示例如下：

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

在上述範例中，本地化物件會定義兩個地區設定( `"en"` 和 `"fr"`)，並為每個地區設定提供兩個使用者介面元素的本地化。

網頁程式碼應將本地化物件傳遞至檢視器建構函式，作為設定物 `localizedTexts` 件欄位的值。 另一個選項是通過調用方法來傳遞定位對 `setLocalizedTexts(localizationInfo)` 像。

支援以下SYMBOL:

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>符號 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 容器。LABEL </span> </p> </td> 
   <td colname="col2"> <p>頂層檢視器元素的ARIA標籤。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>主視圖元件的ARIA角色說明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>ARIA使用提示給鍵盤使用者。 </p> </td> 
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

