---
title: 用戶介面元素本地化
description: 「視訊檢視器」顯示的某些內容可能會受到本地化的限制，包括縮放按鈕和全螢幕按鈕。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: c386a09c-21ce-4105-b416-e6ae50219af0
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# 用戶介面元素本地化{#localization-of-user-interface-elements}

「視訊檢視器」顯示的某些內容可能會受到本地化的限制，包括縮放按鈕和全螢幕按鈕。

檢視器中可本地化的每個文字內容，都會以稱為SYMBOL的特殊檢視器SDK識別碼表示。 任何SYMBOL都具有英語地區( `"en"`)隨現成可用的檢視器提供。 也可以根據需要設定用戶定義的值。

當查看器啟動時，它將檢查當前區域設定，以查看該區域設定的每個支援的SYMBOL是否有用戶定義的值。 若有，則使用使用者定義的值；否則，會回復為現成預設文字。

使用者定義的本地化資料可以以本地化JSON物件的形式傳遞至檢視器。 此類對象包含支援的語言環境清單、每個語言環境的SYMBOL文本值以及預設語言環境。

以下是此類本地化物件的範例：

```
{ 
"en":{ 
"CloseButton.TOOLTIP":"Close", 
"ZoomInButton.TOOLTIP":"Zoom In" 
 }, 
 "fr":{ 
"CloseButton.TOOLTIP":"Fermer", 
"ZoomInButton.TOOLTIP":"Agrandir" 
}, 
defaultLocale:"en" 
}
```

在上例中，本地化物件定義兩個地區設定( `"en"` 和 `"fr"`)，並提供每個地區設定中兩個使用者介面元素的本地化。

網頁代碼應將此類本地化物件傳遞至檢視器建構函式，作為 `localizedTexts` 配置對象的欄位。 替代選項是呼叫 `setLocalizedTexts(localizationInfo)` 方法。

支援下列SYMBOL:

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>符號 </p> </th> 
   <th colname="col2" class="entry"> <p>工具提示…… </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 容器.LABEL </span> </p> </td> 
   <td colname="col2"> <p>頂層檢視器元素的ARIA標籤。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZOOMView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>主要檢視元件的ARIA角色說明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>鍵盤用戶的ARIA使用提示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CloseButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>關閉按鈕。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomInButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>放大按鈕。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomOutButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>縮小按鈕。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomResetButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>縮放重設按鈕。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>全螢幕按鈕處於正常狀態。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>全螢幕狀態的全螢幕按鈕。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>向左滾動按鈕。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>向右滾動按鈕。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>向上捲動按鈕。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>向下捲動按鈕。 </p> </td> 
  </tr> 
 </tbody> 
</table>
