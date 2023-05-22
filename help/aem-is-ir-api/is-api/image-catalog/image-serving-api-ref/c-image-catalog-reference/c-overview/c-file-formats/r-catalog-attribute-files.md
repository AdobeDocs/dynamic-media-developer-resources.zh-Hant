---
description: 目錄屬性檔案可以具有任何名稱，但必須具有.ini檔案尾碼。 可以使用任何文本編輯器輕鬆地維護它們。
solution: Experience Manager
title: 目錄屬性檔案
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 79d9439d-7749-4ae1-aa73-e88e01cf7555
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---

# 目錄屬性檔案{#catalog-attribute-files}

目錄屬性檔案可以具有任何名稱，但必須具有.ini檔案尾碼。 可以使用任何文本編輯器輕鬆地維護它們。

目錄屬性檔案由一組文本記錄組成，用單個文本記錄分隔 `<CR>` （ASCII代碼） `0xD`)，單個 `<LF>` （ASCII代碼） `0xA`)或 `<CR><LF>` 對。 每個記錄都由屬性名稱和一個或多個逗號分隔的屬性值組成：

`*`名稱`*= *`值`*{<CR>|<LF>|<CR><LF }`

<table id="simpletable_0F879121670046AE9414298725961303"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 數值</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 谷</span>[,<span class="varname"> 值</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 名稱</span> </p> </td> 
  <td class="stentry"> <p>屬性名稱。 可以包含一個或多個字母、數字、 — 和_。 不區分大小寫。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 谷</span> </p></td> 
  <td class="stentry"> <p>屬性值。 不得包括 <span class="codeph"> &lt;cr&gt;</span> 或 <span class="codeph"> &lt;lf&gt;</span> 字元，除非在換行符前用單個反斜線轉義。 </p></td> 
 </tr> 
</table>

標籤之間的空格是可選的。

屬性名稱未知的記錄被 [!DNL Platform Server]。

屬性名稱可能由ASCII字母、數字以及&quot;-&quot;、&quot;_&quot;和&quot;。&quot;的任意組合組成。

如果同一屬性檔案中出現多個相同的屬性名稱，則最後一次出現。

使用#作為第一個字元將任何記錄標籤為注釋，解析器將忽略該注釋。
