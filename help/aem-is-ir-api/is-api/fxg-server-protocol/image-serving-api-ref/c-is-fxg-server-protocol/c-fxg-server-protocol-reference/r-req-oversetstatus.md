---
description: 請求類型. 指定要求的類型。
solution: Experience Manager
title: 請求
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 9242c873-5a85-4ede-82b6-4ef15feecf50
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 3%

---

# 請求{#req}

請求類型. 指定要求的類型。

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
   <td colname="col2"> <p> 傳回使用提供的url修飾元轉譯fxg時發生的任何錯誤。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 內容</span> </p> </td> 
   <td colname="col2"> <p> 返回具有<span class="codeph"> s7:element</span>屬性值的所有元素的xml清單以及fxg文檔中所有頁的清單。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oversetstatus</span> </p> </td> 
   <td colname="col2"> <p>傳回XML清單，其中<span class="codeph"> &lt;RichText/&gt;</span>元素被覆集。 </p> <p>傳回為在用戶端上處理而過度設定的<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>元素的xml清單。 只會傳回覆寫的<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>元素。 <span class="+ topic/ph pr-d/codeph codeph"> s7:</span> 使用req=oversetstatus時， <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> elementidis為 <span class="+ topic/ph pr-d/codeph codeph"> 必要屬性</span>。未列出任何不含<span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>的覆蓋集<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>元素。 清單中的每個<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>元素都有<span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>、<span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span>和溢排文字框架的邊界框。 <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span>屬性指示文章中的文本索引，文本可以在框架中裝入到該索引。 <span class="+ topic/ph pr-d/codeph codeph"> Req=</span> oversetstatusus僅適用於 <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 請求的FXG中的元素。它不會列出任何嵌入FXG中的任何<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>元素。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 存在</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>reqId唯一請求標識符 </p> <p>傳回名為catalogRecord.exists的單一屬性。 如果指定的目錄條目存在於影像或預設目錄中，則屬性值將設定為"1"，否則將設定為"0"。 針對/is/content上下文的req=exists請求將指示靜態內容目錄中是否存在指定記錄。 </p> </td> 
  </tr> 
 </tbody> 
</table>
