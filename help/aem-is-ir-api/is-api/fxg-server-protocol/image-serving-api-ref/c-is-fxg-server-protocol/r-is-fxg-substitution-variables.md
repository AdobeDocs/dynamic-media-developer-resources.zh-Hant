---
description: 替代變數可用來將請求URL中的值傳輸到儲存在伺服器上的FXG範本。
solution: Experience Manager
title: 替代變數
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 539d8863-e94d-45dc-bb8c-3db7bead0051
TQID: 'https://experienceleague.adobe.com/-IHIbaXxoDEGqbV2inp4RlmWpH-8js7Dn9b-CK1paxg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 117
ht-degree: 0%

---

# 替代變數{#substitution-variables}

替代變數可用來將請求URL中的值傳輸到儲存在伺服器上的FXG範本。

` $ *`var`*= *`value`*`

<table id="simpletable_76B381800C0D411F87CD551FC30B0579"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">變數</span> </span> </p> </td> 
  <td class="stentry"> <p>變數名稱。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">值</span> </span> </p> </td> 
  <td class="stentry"> <p>變數要設定的值（字串）。 </p> </td> 
 </tr> 
</table>

* 變數定義和參考可能會出現在請求URL的查詢部分中。
* 變數的定義如上所述，與其他IS命令類似；前導的「$」會將該命令識別為變數定義。
* 變數名稱`*`var`*`區分大小寫，而且可能由字母、數字、&#39;-&#39;和&#39;_&#39;的任意組合所組成。
* 重要值必須為單次URL編碼，才能安全HTTP傳輸。
