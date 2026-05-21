---
description: 「影像伺服」提供數個轉譯文字的替代方案，可透過text=和textPs=命令存取。
solution: Experience Manager
title: 文字格式設定
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2c120ed1-b556-4caf-a30e-63ae48cc2104
TQID: 'https://experienceleague.adobe.com/OzCs0opEKfoih79LE4UuXEOJnN4Zh6iBtQNdRxCddAE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 579
ht-degree: 6%

---

# 文字格式設定{#text-formatting}

「影像伺服」提供數個轉譯文字的替代方案，可透過text=和textPs=命令存取。

`textPs=`提供與Adobe Photoshop和Illustrator轉譯的文字高度相似性。 `text=`與使用Windows Wordpad轉譯的文字相當相容。

>[!NOTE]
>
>除了其他部份列出的差異之外，`text=`在轉譯的文字與`textPs=`之間也會產生細微的差異。 例如，底線的粗細和位置不同，合成斜體會以稍微不同的角度呈現。 如果文字不符合可用空間，`text=`可能會部分裁切最後一行，而`textPs=`只會呈現完整的行。

所有文字指令都接受以RTF （RTF格式）規格的子集為基礎的格式化文字。 每個文字圖層可以指定不同的文字指令。

下表列出每個文字指令可用的主要功能：

<table id="table_9C41CBDA94C24805B538E5049B0137C6"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>功能</b> </th> 
   <th class="entry"> <b>文字=</b> </th> 
   <th class="entry"> <b> textPs=</b> </th> 
   <th class="entry"> <b>另請參閱</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> 與Adobe Photoshop相容 </p> </td> 
   <td> <p> 無 </p> </td> 
   <td> <p> 有限 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>將文字排列成任意形狀 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>textFlowPath=， textFlowXPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>沿著任意路徑排列文字 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>文字路徑= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>複製彎管頭 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> 複製彎管頭 <p>, <pre>\組排文字</pre>, <pre>\複製管線</pre>, <pre>\copyfitmaxlines</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>文字方塊邊界 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p><pre>\margl</pre>, <pre>\margr</pre>, <pre>\margt</pre>, <pre>\margb</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>完整的段落齊行 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p><pre>\qj</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>最後一行對齊 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>\lastql， \lastqr， \lastqc， \lastqj </p> </td> 
  </tr> 
  <tr> 
   <td> <p>段落縮排 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>\fi， \li， \ri </p> </td> 
  </tr> 
  <tr> 
   <td> <p>全部大寫字與小型大寫字文字 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>\caps， \scaps </p> </td> 
  </tr> 
  <tr> 
   <td> <p>影像伺服顏色 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>\*\iscolortbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>多重消除鋸齒模式 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>由上到下/由右到左文字排列 </p> </td> 
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
   <td> <p>自動調整圖層大小以符合文字 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>text=，textId=，size= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>CMYK支援 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>\cmykcolortbl， \*\iscolortbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>由右至左字元流程 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>\rtlch </p> </td> 
  </tr> 
  <tr> 
   <td> <p>停用自動換行 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>自動縮放文字以符合圖層（透過改變解析度） </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
 </tbody> 
</table>

RTF相容的字串可以手動組裝，或透過在能儲存RTF檔案的文字編輯器或文書處理器中格式化所要的文字來組裝。 然後可以使用純文字編輯器開啟RTF檔案，並將檔案的相關原始RTF內容複製到請求URL。

有些文書處理器會產生相當大型的檔案，其中包括Dynamic Media影像伺服未使用的重大前導碼。 建議先從字串中移除未使用的RTF元素，然後再將字串傳遞至文字命令。

RTF字串支援以UTF-8和ISO標準為基礎的語言編碼，作為標準RTF字元編碼機制的替代方案。 這可讓應用程式在不瞭解RTF編碼的情況下將非英文文字傳送至伺服器。

如果要透過http傳輸字串，所有非HTTP相容的字元都必須適當地逸出。 如果字串已併入影像目錄記錄的`catalog::Modifiers`欄位中，則只需要逸出&#39;=&#39;、&#39;&amp;&#39;和&#39;%&#39;。 控制字元（包括`<CR>`、`<LF>`和`<TAB>`）一律應移除。

「影像伺服」文字引擎會解譯RTF規格1.6版所定義的命令子集。 此子集著重於字型/字元格式、簡單的段落格式，以及支援國際字型和字元集。 目前不支援更進階的格式建構，例如樣式表和表格。

嘗試手動建構RTF編碼的文字字串時，需要熟悉Microsoft所發佈的RTF規格。

* [字型處理](r-font-handling.md)
* [色彩處理](r-color-handling.md)
* [複製彎管頭](r-copy-fitting.md)
* [文字圖層](r-text-layers.md)
* [文字定位](r-text-positioning.md)
* [保留的字元](r-reserved-characters.md)
* [支援的RTF命令和關鍵字](c-supported-rtf-commands-and-keywords/c-supported-rtf-commands-and-keywords.md)
* [RTF編碼範例](r-rtf-encoding-examples.md)
