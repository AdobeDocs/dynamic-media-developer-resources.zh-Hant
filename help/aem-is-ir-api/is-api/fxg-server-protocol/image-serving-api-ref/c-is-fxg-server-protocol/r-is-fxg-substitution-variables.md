---
description: 替代變數可用來將值從請求URL傳輸至儲存在伺服器上的FXG範本。
solution: Experience Manager
title: 替代變數
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 539d8863-e94d-45dc-bb8c-3db7bead0051
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '120'
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
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>變數要設定的值（字串）。 </p> </td> 
 </tr> 
</table>

* 變數定義和參考可能發生在請求URL的查詢部分。
* 變數定義如上，與其他IS命令類似；前導「$」將命令標識為變數定義。
* 變數名稱`*`var`*`區分大小寫，可能包含字母、數字、「 — 」和「_」的任意組合。
* 重要值必須是單通URL編碼，才能安全HTTP傳輸。
