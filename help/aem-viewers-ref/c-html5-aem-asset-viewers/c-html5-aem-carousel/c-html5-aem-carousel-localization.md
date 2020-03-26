---
description: 轉盤檢視器顯示的某些內容可能會受當地語系限制。 這包括投影片導覽按鈕。
seo-description: 轉盤檢視器顯示的某些內容可能會受當地語系限制。 這包括投影片導覽按鈕。
seo-title: 使用者介面元素的本地化
solution: Experience Manager
title: 使用者介面元素的本地化
topic: Dynamic media
uuid: 82e4dc72-cc12-4ab5-8370-6270f9a3d45f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 使用者介面元素的本地化{#localization-of-user-interface-elements}

轉盤檢視器顯示的某些內容可能會受當地語系限制。 這包括投影片導覽按鈕。

檢視器中可本地化的每個文字內容，都會以稱為SYMBOL的特殊檢視器SDK識別碼來表示。 任何SYMBOL都具有隨附於現成可用檢視器的英文地區( `"en"`)的預設相關文字值，也可針對所需的地區設定使用者定義的值。

當檢視器啟動時，會檢查目前的地區設定，以查看每個支援的SYMBOL是否都有使用者定義的值。 若有，則使用使用者定義的值；否則，它會回到預設的預設文字。

使用者定義的本地化資料可以作為本地化JSON物件傳遞至檢視器。 此類對象包含支援的語言環境清單、每個語言環境的SYMBOL文本值以及預設語言環境。

此類本地化對象的示例如下：

```
{ 
"en":{ 
"PanLeftButton.TOOLTIP":"Left", 
"PanRightButton.TOOLTIP":"Right" 
 }, 
 "fr":{ 
"PanLeftButton.TOOLTIP":"Gauchiste", 
"PanRightButton .TOOLTIP":"Droit" 
}, 
defaultLocale:"en" 
}
```

在上述範例中，本地化物件會定義兩個地區設定( `"en"` 和 `"fr"`)，並為每個地區設定中的兩個使用者介面元素提供本地化。

網頁程式碼應將本地化物件傳遞至檢視器建構函式，做為設定物 `localizedTexts` 件欄位的值。 另一種選擇是通過調用方法傳遞定位 `setLocalizedTexts(localizationInfo)` 對象。

支援以下SYMBOL:

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>符號 </p> </th> 
   <th colname="col2" class="entry"> <p>工具提示…… </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>選取的播放暫停按鈕狀態。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>未選取的播放暫停按鈕狀態。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CAROUSELVIEWER_TOOLTIP_GOTO </span> </p> </td> 
   <td colname="col2"> <p> 用於上一個和下一個投影片按鈕的工具提示和ARIA標籤。 </p> <p>接受兩個取代Token: <span class="codeph"> 當前幻燈片索 </span> 引為$CURRENT_FRAME$，投 <span class="codeph"> 影片總數為$TOTAL_FRAMES </span> $。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 容器。LABEL </span> </p> </td> 
   <td colname="col2"> <p> 頂層檢視器元素的ARIA標籤。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 轉盤檢視。ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p> 主視圖元件的ARIA角色說明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CarouselView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p> ARIA使用提示給鍵盤使用者。 </p> </td> 
  </tr> 
 </tbody> 
</table>

