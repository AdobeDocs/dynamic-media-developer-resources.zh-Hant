---
title: 用戶介面元素的本地化
description: 「基本縮放查看器」顯示的某些內容受本地化的限制，包括縮放按鈕和全屏按鈕。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 8c399b64-e278-41bc-a9eb-692812979fea
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 0%

---

# 用戶介面元素的本地化{#localization-of-user-interface-elements}

「基本縮放查看器」顯示的某些內容受本地化的限制，包括縮放按鈕和全屏按鈕。

可本地化的查看器中的每個文本內容都由稱為SYMBOL的特殊查看器SDK標識符表示。 任何SYMBOL都具有英語區域設定的預設關聯文本值( `"en"`)，並且可能還根據需要為任意多個區域設定用戶定義的值。

當查看器啟動時，它將檢查當前區域設定，以查看區域設定中每個支援的SYMBOL是否有用戶定義的值。 如果存在，則使用用戶定義的值；否則，它會回退到現成的預設文本。

用戶定義的本地化資料可以作為本地化JSON對象傳遞給查看器。 此類對象包含支援的語言環境清單、每個語言環境的SYMBOL文本值和預設語言環境。

此類本地化對象的示例：

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

在上例中，本地化對象定義兩個區域設定( `"en"` 和 `"fr"`)，並為每個區域設定中的兩個用戶介面元素提供本地化。

網頁代碼應將此本地化對象作為值傳遞給查看器建構子 `localizedTexts` 的子菜單。 另一種選擇是通過調用 `setLocalizedTexts(localizationInfo)` 的雙曲餘切值。

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
   <td colname="col1"> <p> <span class="codeph"> 容器.LABEL </span> </p> </td> 
   <td colname="col2"> <p>頂級查看器元素的ARIA標籤。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>主視圖元件的ARIA角色說明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>鍵盤用戶的ARIA用法提示。 </p> </td> 
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
   <td colname="col2"> <p>縮放重置按鈕。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>全屏按鈕處於正常狀態。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>全屏狀態的全屏按鈕。 </p> </td> 
  </tr> 
 </tbody> 
</table>
