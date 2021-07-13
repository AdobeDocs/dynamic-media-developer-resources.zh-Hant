---
description: 「互動式影像檢視器」所顯示的某些內容可能會受到本地化的規範。 這包括使用者介面元素工具提示，以及由載入時彈出縮放檢視顯示的資訊訊息。
title: 用戶介面元素本地化
feature: Dynamic Media Classic，檢視器， SDK/API，互動式影像
role: Developer,User
exl-id: 19749c74-5c31-4dcf-ab07-0e7f10176a86
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 0%

---

# 用戶介面元素本地化{#localization-of-user-interface-elements}

「互動式影像檢視器」所顯示的某些內容可能會受到本地化的規範。 這包括使用者介面元素工具提示，以及由載入時彈出縮放檢視顯示的資訊訊息。

檢視器中可本地化的每個文字內容，都會以稱為SYMBOL的特殊檢視器SDK識別碼表示。 任何SYMBOL都具有隨現成查看器提供的英語語言環境(`"en"`)的預設關聯文本值，並且還可以根據需要設定任意數量的語言環境的用戶定義值。

當查看器啟動時，它將檢查當前區域設定，以查看此區域設定的每個支援的SYMBOL是否有用戶定義的值。 若有，則使用使用者定義的值；否則，會回復為現成預設文字。

使用者定義的本地化資料可以以本地化JSON物件的形式傳遞至檢視器。 此類對象包含支援的語言環境清單、每個語言環境的SYMBOL文本值以及預設語言環境。

以下是此類本地化物件的範例：

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

在上例中，本地化對象定義了兩個區域設定（`"en"`和`"fr"`），並為每個區域設定中的兩個用戶介面元素提供本地化。

網頁代碼應將本地化對象作為配置對象的`localizedTexts`欄位的值傳遞給查看器建構子。 替代選項是呼叫`setLocalizedTexts(localizationInfo)`方法以傳遞本地化物件。

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
   <td colname="col1"> <p> <span class="codeph"> 容器.LABEL  </span> </p> </td> 
   <td colname="col2"> <p>頂層檢視器元素的ARIA標籤。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZOOMView.ROLE_DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>主要檢視元件的ARIA角色說明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.USAGE_HINT  </span> </p> </td> 
   <td colname="col2"> <p>鍵盤用戶的ARIA使用提示。 </p> </td> 
  </tr> 
 </tbody> 
</table>
