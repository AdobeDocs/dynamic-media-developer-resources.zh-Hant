---
description: 目錄屬性檔案可以有任何名稱，但必須有。ini檔案尾碼。 使用任何文字編輯器都可輕鬆維護。
seo-description: 目錄屬性檔案可以有任何名稱，但必須有。ini檔案尾碼。 使用任何文字編輯器都可輕鬆維護。
seo-title: 目錄屬性檔案
solution: Experience Manager
title: 目錄屬性檔案
topic: Scene7 Image Serving - Image Rendering API
uuid: ea2bddad-2c4a-43c1-9b62-6e724fcfb8a0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 目錄屬性檔案{#catalog-attribute-files}

目錄屬性檔案可以有任何名稱，但必須有。ini檔案尾碼。 使用任何文字編輯器都可輕鬆維護。

目錄屬性檔案由一組文本記錄組成，由單個 `<CR>` （ASCII代碼0xD）、單個 `<LF>` （ASCII代碼0xA）或對分 `<CR><LF>` 隔。 每個記錄都由屬性名稱和一個或多個逗號分隔的屬性值組成：

` *``*= *``*&#42;[, *`namevaluevalue`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 名 <span class="varname"> 稱 </span></span> </p> </td> 
  <td class="stentry"> <p>屬性名稱；可以由一或多個字母、數字、'-'和'_'組成；不區分大小寫。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 值 <span class="varname"></span></span> </p> </td> 
  <td class="stentry"> <p>屬性值；不得包 <span class="codeph"> 含&lt;CR&gt; </span>或 <span class="codeph"></span> &lt;LF&gt;字元，除非在新行字元之前以單反斜線逸出。 </p> </td> 
 </tr> 
</table>

* Token之間的空格是選用的。
* 平台伺服器將忽略屬性名稱未知的記錄。
* 屬性名稱可能由ASCII字母、數字以及&quot;-&quot;、&quot;_&quot;和&quot;。&quot;的任意組合組成。
* 如果相同的屬性名稱在同一屬性檔案中發生多次，則最後一次出現的屬性名稱會優先。
* 使用&#39;#&#39;作為第一個字元，將解析器忽略的任何記錄標示為注釋。

