---
description: 替代變數可用來將值從請求URL傳輸至儲存在伺服器上的FXG範本。
solution: Experience Manager
title: 替代變數
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---


# 替代變數{#substitution-variables}

替代變數可用來將值從請求URL傳輸至儲存在伺服器上的FXG範本。

` $ *``*= *`varvalue`*`

<table id="simpletable_76B381800C0D411F87CD551FC30B0579"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var  </span> </span> </p> </td> 
  <td class="stentry"> <p>變數名稱。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 值  </span> </span> </p> </td> 
  <td class="stentry"> <p>變數要設定的值（字串）。 </p> </td> 
 </tr> 
</table>

* 變數定義和參考可能發生在請求URL的查詢部分。
* 變數定義如下，類似於其他IS命令；前導&#39;$&#39;會將命令識別為變數定義。
* 變數名稱`*`var`*`區分大小寫，且可由字母、數字、&#39;-&#39;和&#39;_&#39;的任意組合組成。
* 重要值必須是單一傳遞URL編碼，才能安全傳輸HTTP。

