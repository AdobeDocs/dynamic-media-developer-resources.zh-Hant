---
description: 請求類型. 指定請求的類型。
solution: Experience Manager
title: requin
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 3%

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
   <td colname="col2"> <p> 傳回具有<span class="codeph"> s7:element</span>屬性值的所有元素的xml清單，以及fxg檔案中所有頁面的清單。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oversetstatus</span> </p> </td> 
   <td colname="col2"> <p>傳回<span class="codeph"> &lt;RichText/&gt;</span>元素溢排的XML清單。 </p> <p>傳回在用戶端進行溢排處理之<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>元素的xml清單。 只會傳回溢排的<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>元素。 <span class="+ topic/ph pr-d/codeph codeph"> s7:</span> elementidis a required  <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> attribute when using  <span class="+ topic/ph pr-d/codeph codeph"> req=oversetstatus</span>.未列出任何不含<span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>的溢排<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>元素。 清單中的每個<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>元素都有<span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>、<span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span>，以及溢排文字框的邊框。 <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span>屬性會指出內文中的文字索引，最後文字可以符合影格。 <span class="+ topic/ph pr-d/codeph codeph"> Req=</span> oversetstatus僅適用於所 <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 請求FXG中的元素。它不會列出任何內嵌FXG的<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>元素。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 存在</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>reqId唯一請求識別碼 </p> <p>傳回名為catalogRecord.exists的單一屬性。 如果指定的目錄條目存在於映像或預設目錄中，則屬性值設定為"1"，否則設定為"0"。 針對/is/content上下文的req=exists請求將指示靜態內容目錄中是否存在指定記錄。 </p> </td> 
  </tr> 
 </tbody> 
</table>

