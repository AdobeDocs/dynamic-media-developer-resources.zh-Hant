---
title: 目錄屬性檔案
description: 目錄屬性檔案可以有任何名稱，但必須有.ini檔案字尾。 您可以使用任何文字編輯器隨時維護這些標籤。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b5afb99-3201-4e43-93e7-e8998354204f
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---

# 目錄屬性檔案{#catalog-attribute-files}

目錄屬性檔案可以有任何名稱，但必須有 `.ini` 檔案字尾。 您可以使用任何文字編輯器隨時維護這些標籤。

目錄屬性檔案包含一組文字記錄，並以單一檔案分隔 `<CR>` （ASCII代碼0xD），單 `<LF>` （ASCII代碼0xA）或 `<CR><LF>` 配對。 每個記錄都包含一個屬性名稱以及一或多個以逗號分隔的屬性值：

`*`名稱`*= *`值`*&#42;[, *`值`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 名稱 </span> </span> </p> </td> 
  <td class="stentry"> <p>屬性名稱；可能包含一或多個字母、數字、- （連字型大小）和_ （底線）；不區分大小寫。</p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 值 </span> </span> </p> </td> 
  <td class="stentry"> <p>屬性值；不得包含 <span class="codeph"> &lt;cr&gt; </span>，或 <span class="codeph"> &lt;lf&gt; </span> 字元，除非在新行字元前有一個反斜線逸出。 </p> </td> 
 </tr> 
</table>

* Token之間的空白字元為選用。
* 此 [!DNL Platform Server] 會忽略具有未知屬性名稱的記錄。
* 屬性名稱可包含ASCII字母、數字和 `-`， `_`、和 `.` 個字元。
* 如果相同的屬性名稱在相同的屬性檔案中出現多次，則會以最後一個出現的屬性名稱為準。
* 使用 `#` 做為第一個字元，可將任何記錄標籤為剖析器忽略的註解。
