---
description: 互動式影像檢視器顯示的某些內容可能會受當地語系限制。 這包括使用者介面元素工具提示和載入時彈出縮放檢視所顯示的資訊訊息。
seo-description: 互動式影像檢視器顯示的某些內容可能會受當地語系限制。 這包括使用者介面元素工具提示和載入時彈出縮放檢視所顯示的資訊訊息。
seo-title: 使用者介面元素的本地化
title: 使用者介面元素的本地化
uuid: 1a22570b-8435-4e57-a022-34428bddc7f7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 使用者介面元素的本地化{#localization-of-user-interface-elements}

互動式影像檢視器顯示的某些內容可能會受當地語系限制。 這包括使用者介面元素工具提示和載入時彈出縮放檢視所顯示的資訊訊息。

檢視器中可本地化的每個文字內容，都會以稱為SYMBOL的特殊檢視器SDK識別碼來表示。 任何SYMBOL都具有隨附於現成可用檢視器的英文地區( `"en"`)的預設相關文字值，也可針對所需的地區設定使用者定義的值。

當檢視器啟動時，會檢查目前的地區設定，以查看每個支援的SYMBOL是否都有使用者定義的值。 若有，則使用使用者定義的值；否則，它會回到預設的預設文字。

使用者定義的本地化資料可以作為本地化JSON物件傳遞至檢視器。 此類對象包含支援的語言環境清單、每個語言環境的SYMBOL文本值以及預設語言環境。

此類本地化對象的示例如下：

```
{ 
"en":{ 
"Container.LABEL":"Interactive Image Viewer" 
 }, 
 "fr":{ 
"Container.LABEL":"Visionneuse d'images interactive" 
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
   <td colname="col1"> <p> <span class="codeph"> 容器。LABEL </span> </p> </td> 
   <td colname="col2"> <p>頂層檢視器元素的ARIA標籤。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>主視圖元件的ARIA角色說明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>ARIA使用提示給鍵盤使用者。 </p> </td> 
  </tr> 
 </tbody> 
</table>

