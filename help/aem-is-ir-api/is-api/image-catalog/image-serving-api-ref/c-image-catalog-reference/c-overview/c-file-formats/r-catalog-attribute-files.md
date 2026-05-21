---
description: 目錄屬性檔案可以有任何名稱，但必須有.ini檔案字尾。 您可以使用任何文字編輯器隨時維護這些標籤。
solution: Experience Manager
title: 目錄屬性檔案
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 79d9439d-7749-4ae1-aa73-e88e01cf7555
TQID: 'https://experienceleague.adobe.com/RCxeXg3wb10jo37biAs1puqmEo8bAL-i-oZBwGHuloA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 195
ht-degree: 0%

---

# 目錄屬性檔案{#catalog-attribute-files}

目錄屬性檔案可以有任何名稱，但必須有.ini檔案字尾。 您可以使用任何文字編輯器隨時維護這些標籤。

目錄屬性檔案包含一組文字記錄，由單一`<CR>` （ASCII代碼`0xD`）、單一`<LF>` （ASCII代碼`0xA`）或`<CR><LF>`配對分隔。 每個記錄都包含一個屬性名稱以及一或多個以逗號分隔的屬性值：

`*`名稱`*= *`值`*{<CR>|<LF>|<CR><LF }`

<table id="simpletable_0F879121670046AE9414298725961303"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">值</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span>[，<span class="varname">值</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">名稱</span> </p> </td> 
  <td class="stentry"> <p>屬性名稱。 可能包含一或多個字母、數字、 — 和_。 不區分大小寫。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">值</span> </p></td> 
  <td class="stentry"> <p>屬性值。 不得包含<span class="codeph"> &lt;CR&gt;</span>或<span class="codeph"> &lt;LF&gt;</span>個字元，除非在新行字元前有一個反斜線逸出。 </p></td> 
 </tr> 
</table>

Token之間的空白字元為選用。

[!DNL Platform Server]會忽略具有未知屬性名稱的記錄。

屬性名稱可包含ASCII字母、數字，以及「 — 」、「_」和「。」的任意組合。

如果相同的屬性名稱在相同的屬性檔案中出現多次，則會以最後一個出現的屬性名稱為準。

使用#作為第一個字元，將任何記錄標籤為註解，解析器會忽略該註解。
