---
description: 目錄屬性檔案可以有任何名稱，但必須有.ini檔案尾碼。 可使用任何文字編輯器輕鬆維護這些文字。
solution: Experience Manager
title: 目錄屬性檔案
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 79d9439d-7749-4ae1-aa73-e88e01cf7555
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 1%

---

# 目錄屬性檔案{#catalog-attribute-files}

目錄屬性檔案可以有任何名稱，但必須有.ini檔案尾碼。 可使用任何文字編輯器輕鬆維護這些文字。

目錄屬性檔案由一組文本記錄組成，以單個 `<CR>` (ASCII碼 `0xD`)，單一 `<LF>` (ASCII碼 `0xA`)或 `<CR><LF>` 配對。 每個記錄都包含屬性名稱和一或多個逗號分隔的屬性值：

`*`名稱`*= *`值`*{<CR>|<LF>|<CR><LF }`

<table id="simpletable_0F879121670046AE9414298725961303"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> values</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span>[,<span class="varname"> 值</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 名稱</span> </p> </td> 
  <td class="stentry"> <p>屬性名稱。 可能包含一個或多個字母、數字、 — 和_。 不區分大小寫。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>屬性值。 不得包括 <span class="codeph"> &lt;cr&gt;</span> 或 <span class="codeph"> &lt;lf&gt;</span> 字元，除非在新行字元前面以單反斜線逸出。 </p></td> 
 </tr> 
</table>

代號之間的空白字元為選用。

屬性名稱未知的記錄會被 [!DNL Platform Server].

屬性名稱可以包含ASCII字母、數字以及「 — 」、「_」和「。」的任意組合。

如果同一屬性檔案中出現多次相同的屬性名稱，則最後一個名稱優先。

使用#作為第一個字元，將任何記錄標籤為注釋，解析器將其忽略。
