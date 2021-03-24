---
description: 目錄屬性檔案可以有任何名稱，但必須有。ini檔案尾碼。 使用任何文字編輯器都可輕鬆維護。
solution: Experience Manager
title: 目錄屬性檔案
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 0%

---


# 目錄屬性檔案{#catalog-attribute-files}

目錄屬性檔案可以有任何名稱，但必須有。ini檔案尾碼。 使用任何文字編輯器都可輕鬆維護。

目錄屬性檔案由一組文本記錄組成，由單個`<CR>`（ASCII代碼0xD）、單個`<LF>`（ASCII代碼0xA）或`<CR><LF>`對分隔。 每個記錄都由屬性名稱和一個或多個逗號分隔的屬性值組成：

`*``*= *``*&#42;[, *`namevaluevalue`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 名稱  </span> </span> </p> </td> 
  <td class="stentry"> <p>屬性名稱；可以由一或多個字母、數字、'-'和'_'組成；不區分大小寫。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 值  </span> </span> </p> </td> 
  <td class="stentry"> <p>屬性值；不得包含<span class="codeph"> &lt;CR&gt; </span>或<span class="codeph"> &lt;LF&gt; </span>字元，除非在新行字元之前以單反斜線逸出。 </p> </td> 
 </tr> 
</table>

* Token之間的空格是選用的。
* 平台伺服器將忽略屬性名稱未知的記錄。
* 屬性名稱可能由ASCII字母、數字以及&quot;-&quot;、&quot;_&quot;和&quot;。&quot;的任意組合組成。
* 如果相同的屬性名稱在同一屬性檔案中發生多次，則最後一次出現的屬性名稱會優先。
* 使用&#39;#&#39;作為第一個字元，將解析器忽略的任何記錄標示為注釋。

