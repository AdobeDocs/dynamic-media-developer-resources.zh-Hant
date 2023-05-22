---
description: Image Serving提供了幾種呈現文本的替代方法，可通過text=和textPs=命令訪問。
solution: Experience Manager
title: 文本格式
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2c120ed1-b556-4caf-a30e-63ae48cc2104
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '557'
ht-degree: 7%

---

# 文本格式{#text-formatting}

Image Serving提供了幾種呈現文本的替代方法，可通過text=和textPs=命令訪問。

`textPs=` 提供與Adobe Photoshop和Illustrator所呈現的文本的高度相似性。 `text=` 與Windows寫字板呈現的文本相當相容。

>[!NOTE]
>
>除了其他地方列出的差異外， `text=` 與 `textPs=`。 例如，下划線的厚度和位置不相同，合成斜體以略微不同的角度呈現。 如果文本不適合可用空間， `text=` 可能會部分裁剪最後一行，而 `textPs=` 將僅呈現完整行。

所有文本命令都接受基於RTF（RTF格式）規範子集的格式化文本。 每個文本層可以指定不同的文本命令。

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
   <td> <p>textFlowPath=,textFlowXPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>沿任意路徑流文本 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>textPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>複製管接頭 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> 複製管接頭 <p>, <pre>\副本</pre>, <pre>\折線</pre>, <pre>\copfitmaxlines</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>文本框邊距 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p><pre>\margl</pre>, <pre>\margr</pre>, <pre>\marg</pre>, <pre>\margb</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>段落全文理由 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p><pre>\qj</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>最後一行說明 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>\lastql, \lastqr, \lastqc, \lastqj </p> </td> 
  </tr> 
  <tr> 
   <td> <p>段落縮進 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>\fi, \li, \ri </p> </td> 
  </tr> 
  <tr> 
   <td> <p>所有大寫和小寫文本 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>\caps,\caps </p> </td> 
  </tr> 
  <tr> 
   <td> <p>影像服務顏色 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>\*\iscolorbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>多種消除鋸齒模式 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>上下/右左文本流 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>\stext流 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Photofont®支援 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> 字型處理 </td> 
  </tr> 
  <tr> 
   <td> <p>自動調整圖層大小以適合文本 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>text=,textId=,size= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>CMYK支援 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>\cmykcoltortbl, \*\iscolorbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>從右到左字元流 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>\rtch </p> </td> 
  </tr> 
  <tr> 
   <td> <p>禁用換行 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>自動縮放文本以適合圖層（通過改變解析度） </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
 </tbody> 
</table>

可以手動裝配符合RTF的字串，或通過在能夠保存RTF檔案的文本編輯器或字處理器中格式化所需文本來裝配。 然後，RTF檔案可以在純文字檔案編輯器中開啟，並將檔案的相關原始RTF內容複製到請求URL。

一些字處理器生成較大的檔案，其中包括Dynamic Media影像服務未使用的大量前導碼。 建議先從字串中刪除未使用的RTF元素，然後再將字串傳遞給text命令。

RTF字串支援基於UTF-8和ISO標準的語言編碼，作為標準RTF字元編碼機制的替代方法。 這允許應用程式在不知道RTF編碼的情況下將非英文文本發送到伺服器。

如果要通過http傳輸字串，則必須正確轉義所有非HTTP相容字元。 如果將字串合併到 `catalog::Modifiers` 影像目錄記錄的欄位。 控制字元，包括 `<CR>`。 `<LF>`, `<TAB>` 應始終刪除。

影像服務文本引擎解釋由RTF(RTF)規範1.6版定義的子命令集。此子集側重於字型/字元格式、簡單的段落格式以及對國際字型和字元集的支援。 目前不支援更高級的格式結構，如樣式表和表格。

嘗試手動構造RTF編碼文本字串時，需要熟悉Microsoft發佈的RTF規範。

* [字型處理](r-font-handling.md)
* [顏色處理](r-color-handling.md)
* [複製管接頭](r-copy-fitting.md)
* [文本圖層](r-text-layers.md)
* [文本定位](r-text-positioning.md)
* [保留字元](r-reserved-characters.md)
* [支援的RTF命令和關鍵字](c-supported-rtf-commands-and-keywords/c-supported-rtf-commands-and-keywords.md)
* [RTF編碼示例](r-rtf-encoding-examples.md)
