---
description: 「影像伺服」提供多種轉換文字的替代方式，可透過text=和textPs=指令存取。
solution: Experience Manager
title: 文字格式
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '565'
ht-degree: 7%

---


# 文本格式{#text-formatting}

「影像伺服」提供多種轉換文字的替代方式，可透過text=和textPs=指令存取。

`textPs=` 提供與Adobe Photoshop和Illustrator所轉譯的文字高度相似的內容。`text=` 與使用Windows Wordpad轉換的文字相容。

>[!NOTE]
>
>除了其他位置列出的差異外，與`textPs=`相比，`text=`在轉換的文本中會產生細微的差異。 例如，下划線的厚度和位置不相同，合成斜體以略微不同的角度顯示。 如果文字不符合可用空間，`text=`可能會部分裁切最後一行，而`textPs=`則只會產生完整的行。

所有文本命令都接受基於RTF(Rich Text Format)規範子集的格式化文本。 每個文本圖層可以指定不同的文本命令。

下表列出了每個文本命令可用的主要功能：

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
   <td> <p>將文字排列成任意形狀 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>textFlowPath=,textFlowXPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>沿任意路徑排文 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>textPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>複製調整 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> 複製調整 <p>的 <pre>\copyfit</pre>的 <pre>\copyfitlines</pre>的 <pre>\copyfitmaxlines</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>文字方塊邊界 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p><pre>\margl</pre>的 <pre>\margr</pre>的 <pre>\margt</pre>的 <pre>\margb</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>完整段落論證 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p><pre>\qj</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>最後一行對齊 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>\lastql、\lastqr、\lastqc和\lastqj </p> </td> 
  </tr> 
  <tr> 
   <td> <p>段落縮排 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>\fi, \li, \ri </p> </td> 
  </tr> 
  <tr> 
   <td> <p>所有大寫和小寫文字 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>\caps, \scaps </p> </td> 
  </tr> 
  <tr> 
   <td> <p>影像伺服顏色 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>\*\iscolortbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>多重抗鋸齒模式 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>左上／右文字流 </p> </td> 
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
   <td> <p>自動調整圖層大小以符合文字大小 </p> </td> 
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
   <td> <p>從右到左的字元流 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>\rtlch </p> </td> 
  </tr> 
  <tr> 
   <td> <p>停用換行 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>自動縮放文字以配合圖層（透過各種解析度） </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
 </tbody> 
</table>

RTF相容字串可以手動組合，或在能夠保存RTF檔案的文本編輯器或文字處理器中格式化所需文本。 然後，RTF檔案可以在純文字檔案編輯器中開啟，並將檔案的相關原始RTF內容複製到請求URL。

某些字處理器生成較大的檔案，其中包括Dynamic Media影像服務不使用的大量前導碼。 建議在將字串傳遞到文本命令之前，先從字串中刪除未使用的RTF元素。

RTF字串支援以UTF-8和ISO標準為基礎的語言編碼，以取代標準RTF字元編碼機制。 這樣，應用程式就可以向伺服器發送非英文文本，而不需具備RTF編碼知識。

如果要透過http傳輸字串，所有不符合HTTP的字元都必須正確逸出。 如果字串併入影像目錄記錄的`catalog::Modifiers`欄位，則只需逸出&#39;=&#39;、&#39;&amp;&#39;和&#39;%&#39;。 應一律移除控制字元，包括`<CR>`、`<LF>`和`<TAB>`。

「影像服務」文本引擎解譯由1.6版RTF格式(RTF)規範定義的子命令集。此子集主要針對字型／字元格式、簡單的段落格式，以及支援國際字型和字元集。 目前不支援更進階的格式結構，例如樣式表和表格。

嘗試手動構建RTF編碼文本字串時，需要熟悉Microsoft發佈的RTF格式(RTF)規範。

* [字型處理](r-font-handling.md)
* [色彩處理](r-color-handling.md)
* [複製調整](r-copy-fitting.md)
* [文字圖層](r-text-layers.md)
* [文字定位](r-text-positioning.md)
* [保留字元](r-reserved-characters.md)
* [支援的RTF命令和關鍵字](c-supported-rtf-commands-and-keywords/c-supported-rtf-commands-and-keywords.md)
* [RTF編碼範例](r-rtf-encoding-examples.md)
