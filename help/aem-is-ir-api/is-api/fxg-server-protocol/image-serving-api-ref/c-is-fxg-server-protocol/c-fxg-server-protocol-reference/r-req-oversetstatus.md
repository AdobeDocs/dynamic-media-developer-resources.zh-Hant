---
description: 請求類型. 指定請求的類型。
seo-description: 請求類型. 指定請求的類型。
seo-title: requin
solution: Experience Manager
title: requin
topic: Scene7 Image Serving - Image Rendering API
uuid: 1c8ff9c3-9f39-46a8-bd38-8e0c5ab0f548
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# req{#req}

請求類型. 指定請求的類型。

`req={validate|contents|oversetstatus|exists}`

<table id="table_F39239E5244746DB9F253BB0D5E85D54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 值 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 驗證</span> </p> </td> 
   <td colname="col2"> <p> 傳回使用提供的URL修飾元轉譯fxg時的任何錯誤。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 內容</span> </p> </td> 
   <td colname="col2"> <p> 傳回所有元素的XML清單， <span class="codeph"> 其中包含s7:element</span> 屬性值和fxg檔案中所有頁面的清單。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oversetstatus</span> </p> </td> 
   <td colname="col2"> <p>傳回&lt;RichText/&gt;元 <span class="codeph"> 素溢排的</span> XML清單。 </p> <p>傳回在用戶端上 <span class="+ topic/ph pr-d/codeph codeph"> 進行溢排處理的&lt;RichText/</span> &gt;元素的xml清單。 只 <span class="+ topic/ph pr-d/codeph codeph"> 會傳回溢排</span> 的&lt;RichText/&gt;元素。 <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span> 是使用req=oversetstatus時 <span class="+ topic/ph pr-d/codeph codeph"> 的必要&lt;RichText/</span> &gt; <span class="+ topic/ph pr-d/codeph codeph"> 屬性</span>。 不會列 <span class="+ topic/ph pr-d/codeph codeph"> 出任何不含</span><span class="+ topic/ph pr-d/codeph codeph"> s7:elementid的溢排</span> &lt;RichText/&gt;元素。 清單 <span class="+ topic/ph pr-d/codeph codeph"> 中的每個&lt;RichText/&gt;</span> "元素都有 <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>、 <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span>，以及溢排文字框的邊框。 s7: <span class="+ topic/ph pr-d/codeph codeph"> endCharIndex</span> 屬性會指出文字在文字框中可符合的文字索引。 <span class="+ topic/ph pr-d/codeph codeph"> Req=oversetstatus</span> 僅適用於所請 <span class="+ topic/ph pr-d/codeph codeph"> 求FXG中的&lt;RichText/&gt;</span> elements。 它不會列出任何 <span class="+ topic/ph pr-d/codeph codeph"> 內嵌FXG的&lt;RichText/</span> &gt;元素。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 存在</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>reqId唯一請求識別碼 </p> <p>傳回名為catalogRecord.exists的單一屬性。 如果指定的目錄條目存在於映像或預設目錄中，則屬性值設定為"1"，否則設定為"0"。 針對/is/content上下文的req=exists請求將指示靜態內容目錄中是否存在指定記錄。 </p> </td> 
  </tr> 
 </tbody> 
</table>

