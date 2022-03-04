---
description: 請求類型. 指定請求的類型。
solution: Experience Manager
title: 請求
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9242c873-5a85-4ede-82b6-4ef15feecf50
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 3%

---

# 請求{#req}

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
   <td colname="col2"> <p> 返回使用提供的URL修飾符呈現fxg時的任何錯誤。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 內容</span> </p> </td> 
   <td colname="col2"> <p> 返回所有元素的xml清單 <span class="codeph"> s7：元素</span> 屬性值和fxg文檔中所有頁面的清單。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 溢出狀態</span> </p> </td> 
   <td colname="col2"> <p>返回其的XML清單 <span class="codeph"> &lt;richtext /&gt;</span> 元素被疊加。 </p> <p>返回XML清單 <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 在客戶端處理的元素。 僅 <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 返回溢流的元素。 <span class="+ topic/ph pr-d/codeph codeph"> s7：元素</span> 是必需的 <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 屬性 <span class="+ topic/ph pr-d/codeph codeph"> req=oversetstation</span>。 任意溢流 <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 元素 <span class="+ topic/ph pr-d/codeph codeph"> s7：元素</span> 清單。 每個 <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 清單中的元素具有 <span class="+ topic/ph pr-d/codeph codeph"> s7：元素</span>。 <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span>，以及溢流文本框架的邊框。 的 <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> attribute指示文章中的文本索引，文本可以容納在框架中。 <span class="+ topic/ph pr-d/codeph codeph"> 請求=溢出狀態</span> 僅適用於 <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 請求的FXG中的元素。 它不會列出任何 <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 嵌入的FXG中的元素。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 存在</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>reqId唯一請求標識符 </p> <p>返回名為catalogRecord.exists的單個屬性。 如果映像或預設目錄中存在指定的目錄條目，則將屬性值設定為「1」，否則將其設定為「0」。 針對/is/content上下文的req=exists請求將指示靜態內容目錄中是否存在指定記錄。 </p> </td> 
  </tr> 
 </tbody> 
</table>
