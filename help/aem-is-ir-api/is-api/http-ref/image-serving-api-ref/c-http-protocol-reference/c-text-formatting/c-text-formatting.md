---
description: 「影像伺服」提供多種轉譯文字的替代方式，可透過text=和textPs=命令存取。
solution: Experience Manager
title: 文字格式
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 2c120ed1-b556-4caf-a30e-63ae48cc2104
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '562'
ht-degree: 7%

---

# 文字格式{#text-formatting}

「影像伺服」提供多種轉譯文字的替代方式，可透過text=和textPs=命令存取。

`textPs=` 提供與以Adobe Photoshop和Illustrator轉譯的文字高度的相似度。`text=` 與使用Windows Wordpad呈現的文字相容。

>[!NOTE]
>
>除了其他地方列出的差異外，與`textPs=`相比，`text=`還會在呈現的文本中產生細微差異。 例如，底線沒有相同的厚度和位置，而合成斜體以稍微不同的角度呈現。 如果文字不符合可用空間，`text=`可以部分裁切最後一行，而`textPs=`將僅呈現完整行。

所有文本命令都接受基於RTF（RTF格式）規範的子集的格式化文本。 每個文本層可指定不同的文本命令。

下表列出了每個文本命令可用的關鍵功能：

<table id="table_9C41CBDA94C24805B538E5049B0137C6"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 功能</b> </th> 
   <th class="entry"> <b> 文字=</b> </th> 
   <th class="entry"> <b> textPs=</b> </th> 
   <th class="entry"> <b> 另請參閱</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> Adobe Photoshop相容 </p> </td> 
   <td> <p> 無 </p> </td> 
   <td> <p> 有限 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>將文本流入任意形狀 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>textFlowPath=, textFlowXPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>沿任意路徑流動文本 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>textPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>複製擬合 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> 複製管接頭 <p>, <pre>\copyfit</pre>, <pre>\copyfitlines</pre>, <pre>\copyfitmaxlines</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>文本框邊距 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p><pre>\margl</pre>, <pre>\margr</pre>, <pre>\margt</pre>, <pre>\margb</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>全段理由 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p><pre>\qj</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>最後一行對齊 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>\lastql, \lastqr, \lastqc, \lastqj </p> </td> 
  </tr> 
  <tr> 
   <td> <p>段落縮排 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>\fi, \li, \ri </p> </td> 
  </tr> 
  <tr> 
   <td> <p>全大寫和小大寫文字 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>\caps,\scaps </p> </td> 
  </tr> 
  <tr> 
   <td> <p>影像伺服顏色 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>\*\iscolortbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>多種消除鋸齒模式 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>左上/右文字流 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>\stextFlow </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Photofont®支援 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> 字型處理 </td> 
  </tr> 
  <tr> 
   <td> <p>自動調整圖層大小以適合文字 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>text=, textId=, size= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>CMYK支援 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>\cmykcolortbl, \*\iscolortbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>由右至左字元流 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>\rtlch </p> </td> 
  </tr> 
  <tr> 
   <td> <p>禁用換行 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>自動縮放文字以適合圖層（通過不同解析度） </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
 </tbody> 
</table>

RTF相容字串可以手動組合，或者通過在能夠保存RTF檔案的文本編輯器或文字處理器中格式化所需的文本來組合。 然後，RTF檔案可以在純文字檔案編輯器中開啟，並且檔案的相關原始RTF內容被複製到請求URL中。

某些字處理器生成較大的檔案，這些檔案包括不被Dynamic Media影像服務使用的大量前導碼。 建議先從字串中刪除未使用的RTF元素，然後再將字串傳遞到文本命令。

基於UTF-8和ISO標準的語言編碼支援在RTF字串中，作為標準RTF字元編碼機制的替代。 這允許應用程式向伺服器發送非英語文本，而不需要RTF編碼。

如果要透過http傳輸字串，則所有非HTTP相容字元都必須正確逸出。 如果將字串併入影像目錄記錄的`catalog::Modifiers`欄位，則只需將「=」、「&amp;」和「%」逸出。 應一律移除控制字元，包括`<CR>`、`<LF>`和`<TAB>`。

影像伺服文本引擎解釋由RTF格式(RTF)規範1.6版定義的命令的子集。該子集側重於字型/字元格式、簡單段落格式以及對國際字型和字元集的支援。 目前不支援更進階的格式結構，例如樣式表和表格。

嘗試手動構建RTF編碼文本字串時，需要熟悉Microsoft發佈的RTF格式(RTF)規範。

* [字型處理](r-font-handling.md)
* [色彩處理](r-color-handling.md)
* [複製擬合](r-copy-fitting.md)
* [文字層](r-text-layers.md)
* [文本定位](r-text-positioning.md)
* [保留字元](r-reserved-characters.md)
* [支援的RTF命令和關鍵字](c-supported-rtf-commands-and-keywords/c-supported-rtf-commands-and-keywords.md)
* [RTF編碼示例](r-rtf-encoding-examples.md)
