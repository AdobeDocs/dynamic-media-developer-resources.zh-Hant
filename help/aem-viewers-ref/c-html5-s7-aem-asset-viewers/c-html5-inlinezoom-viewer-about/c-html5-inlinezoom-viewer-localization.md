---
description: 彈出檢視器顯示的某些內容可能會受到本地化規範。 此內容包括用戶介面元素工具提示和資訊消息，這些消息由載入時彈出縮放視圖顯示。
solution: Experience Manager
title: 用戶介面元素本地化
feature: Dynamic Media Classic，檢視器，SDK/API，內嵌縮放
role: Developer,Business Practitioner
exl-id: 49795aa1-07c7-4f2e-bfd9-51d6581898ed
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 0%

---

# 用戶介面元素本地化{#localization-of-user-interface-elements}

彈出檢視器顯示的某些內容可能會受到本地化規範。 此內容包括用戶介面元素工具提示和資訊消息，這些消息由載入時彈出縮放視圖顯示。

檢視器中可本地化的每個文字內容，都會以稱為SYMBOL的特殊檢視器SDK識別碼表示。 任何SYMBOL都具有隨現成查看器提供的英語語言環境(`"en"`)的預設關聯文本值，並且還可以根據需要設定任意數量的語言環境的用戶定義值。

當查看器啟動時，它將檢查當前區域設定，以查看此區域設定的每個支援的SYMBOL是否有用戶定義的值。 若有，則使用使用者定義的值；否則，會回復為現成預設文字。

使用者定義的本地化資料可以以本地化JSON物件的形式傳遞至檢視器。 此類對象包含支援的語言環境清單、每個語言環境的SYMBOL文本值以及預設語言環境。

以下是此類本地化物件的範例：

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

在上例中，本地化對象定義了兩個區域設定（`"en"`和`"fr"`），並為每個區域設定中的兩個用戶介面元素提供本地化。

網頁代碼應將此類本地化對象作為配置對象的`localizedTexts`欄位的值傳遞給查看器建構子。 替代選項是呼叫`setLocalizedTexts(localizationInfo)`方法以傳遞本地化物件。

支援下列SYMBOL:

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>符號 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 容器.LABEL  </span> </p> </td> 
   <td colname="col2"> <p>頂層檢視器元素的ARIA標籤。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.ROLE_DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>主要檢視元件的ARIA角色說明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.USAGE_HINT  </span> </p> </td> 
   <td colname="col2"> <p>鍵盤用戶的ARIA使用提示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_OVER  </span> </p> </td> 
   <td colname="col2"> <p>案頭系統的資訊消息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_TAP  </span> </p> </td> 
   <td colname="col2"> <p>觸控裝置的資訊訊息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>向左滾動按鈕的工具提示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollRightButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>滾動右鍵的工具提示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>向上捲動按鈕的工具提示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>向下捲動按鈕的工具提示。 </p> </td> 
  </tr> 
 </tbody> 
</table>
