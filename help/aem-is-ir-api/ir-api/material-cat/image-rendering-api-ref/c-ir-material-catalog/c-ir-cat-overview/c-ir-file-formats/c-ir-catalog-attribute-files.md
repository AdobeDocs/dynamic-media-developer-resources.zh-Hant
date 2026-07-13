---
title: 目錄屬性檔案
description: 目錄屬性檔案可以有任何名稱，但必須有.ini檔案字尾。 您可以使用任何文字編輯器隨時維護這些標籤。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b5afb99-3201-4e43-93e7-e8998354204f
TQID: 'https://experienceleague.adobe.com/OwtzX3xKh5ByC3eUhz7dmFjGR5HRD9cbE6atUEL0Nic'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 192
ht-degree: 0%

---

# 目錄屬性檔案{#catalog-attribute-files}

目錄屬性檔案可以有任何名稱，但必須有`.ini`個檔案字尾。 您可以使用任何文字編輯器隨時維護這些標籤。

目錄屬性檔案包含一組文字記錄，由單一`<CR>` （ASCII代碼0xD）、單一`<LF>` （ASCII代碼0xA）或`<CR><LF>`配對分隔。 每個記錄都包含一個屬性名稱以及一或多個以逗號分隔的屬性值：

`*`名稱`*= *`值`*&#42;[, *`值`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">名稱</span> </span> </p> </td> 
  <td class="stentry"> <p>屬性名稱；可能包含一或多個字母、數字、- （連字型大小）和_ （底線）；不區分大小寫。</p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">值</span> </span> </p> </td> 
  <td class="stentry"> <p>屬性值；不可包含<span class="codeph"> &lt;CR&gt; </span>或<span class="codeph"> &lt;LF&gt; </span>字元，除非在新行字元前有一個反斜線逸出。 </p> </td> 
 </tr> 
</table>

* Token之間的空白字元為選用。
* [!DNL Platform Server]會忽略具有未知屬性名稱的記錄。
* 屬性名稱可包含ASCII字母、數字和`-`、`_`和`.`字元的任意組合。
* 如果相同的屬性名稱在相同的屬性檔案中出現多次，則會以最後一個出現的屬性名稱為準。
* 使用`#`做為第一個字元，將任何記錄標籤為剖析器忽略的註解。

