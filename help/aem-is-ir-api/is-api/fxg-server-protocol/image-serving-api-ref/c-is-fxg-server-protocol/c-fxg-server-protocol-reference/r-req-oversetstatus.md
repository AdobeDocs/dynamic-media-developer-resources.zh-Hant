---
title: 需要
description: 請求類型. 指定要求的型別。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9242c873-5a85-4ede-82b6-4ef15feecf50
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 3%

---

# 需要{#req}

請求類型. 指定要求的型別。

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
   <td colname="col2"> <p> 傳回使用提供的url修飾元呈現fxg時的任何錯誤。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 內容</span> </p> </td> 
   <td colname="col2"> <p> 傳回所有元素的xml清單，其中包含 <span class="codeph"> s7：element</span> 屬性值和fxg檔案中所有頁面的清單。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oversetstatus</span> </p> </td> 
   <td colname="col2"> <p>傳回XML清單，其中 <span class="codeph"> &lt;richtext /&gt;</span> 元素溢位。 </p> <p>傳回xml清單 <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 在使用者端處理時溢位的元素。 僅限 <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 會傳回溢排的元素。 此 <span class="+ topic/ph pr-d/codeph codeph"> s7：elementid</span> 為必要項 <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 屬性（使用時） <span class="+ topic/ph pr-d/codeph codeph"> req=oversetstatus</span>. 任何溢位 <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 元素沒有 <span class="+ topic/ph pr-d/codeph codeph"> s7：elementid</span> 未列出。 每個 <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 清單中的元素具有 <span class="+ topic/ph pr-d/codeph codeph"> s7：elementid</span>， <span class="+ topic/ph pr-d/codeph codeph"> s7：endCharIndex</span>，以及溢排文字框的邊界方框。 此 <span class="+ topic/ph pr-d/codeph codeph"> s7：endCharIndex</span> attribute表示內文中的文字索引，文字可以容納在框架中。 此 <span class="+ topic/ph pr-d/codeph codeph"> Req=oversetstatus</span> 僅適用於 <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 元素中指定的FXG。 它不會列出任何 <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 任何內嵌FXG中的元素。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 存在</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[，text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>reqId唯一要求識別碼 </p> <p>它會傳回名為catalogRecord.exists的單一屬性。 如果指定的目錄專案存在於影像或預設目錄中，則屬性值會設為「1」，否則會設為「0」。 針對/is/content內容的req=exists要求會指出靜態內容目錄中是否有指定記錄。 </p> </td> 
  </tr> 
 </tbody> 
</table>
