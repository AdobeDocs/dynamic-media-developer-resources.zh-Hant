---
description: 目錄屬性檔案可以有任何名稱，但必須有.ini檔案尾碼。 可使用任何文字編輯器輕鬆維護這些文字。
solution: Experience Manager
title: 目錄屬性檔案
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 79d9439d-7749-4ae1-aa73-e88e01cf7555
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---

# 目錄屬性檔案{#catalog-attribute-files}

目錄屬性檔案可以有任何名稱，但必須有.ini檔案尾碼。 可使用任何文字編輯器輕鬆維護這些文字。

目錄屬性檔案由一組文本記錄組成，由單個`<CR>`（ASCII代碼`0xD`）、單個`<LF>`（ASCII代碼`0xA`）或`<CR><LF>`對分隔。 每個記錄都包含屬性名稱和一或多個逗號分隔的屬性值：

`*``*= *`名稱值`*{<CR>|<LF>|<CR><LF }`

<table id="simpletable_0F879121670046AE9414298725961303"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> values</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span>[,<span class="varname"> values</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 名稱</span> </p> </td> 
  <td class="stentry"> <p>屬性名稱。 可能包含一個或多個字母、數字、 — 和_。 不區分大小寫。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>屬性值。 不得包含<span class="codeph"> &lt;CR&gt;</span>或<span class="codeph"> &lt;LF&gt;</span>字元，除非在新行字元前面用單反斜線逸出。 </p></td> 
 </tr> 
</table>

代號之間的空白字元為選用。

Platform伺服器會忽略屬性名稱未知的記錄。

屬性名稱可以包含ASCII字母、數字以及「 — 」、「_」和「。」的任意組合。

如果同一屬性檔案中出現多次相同的屬性名稱，則最後一個名稱優先。

使用#作為第一個字元，將任何記錄標籤為注釋，解析器將其忽略。
