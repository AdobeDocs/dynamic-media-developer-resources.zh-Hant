---
description: 啟用FXG的最佳化。
solution: Experience Manager
title: enableVisibleAttributeOptimization
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a643694e-f6a2-424e-8f6e-3dbb4cdc41b3
TQID: 'https://experienceleague.adobe.com/QpFJklGLyM9-R9RfGfMQE0mypUKrs-L4g21yWtRyO10'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 96
ht-degree: 2%

---

# enableVisibleAttributeOptimization{#enablevisibleattributeoptimization}

啟用FXG的最佳化。

<table id="simpletable_FDE0D8786BC747AF87A336452500E695"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &amp;enableVisibleAttributeOptimization</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

移除在FXG中可見度設為false的元素，同時傳遞此FXG，進而減少FXG的處理時間。 雖然它只會移除可視性為false的元素，而不會影響FXG中的任何其他元素。 例如，如果`Path`上有文字，且`Path`的可見度設定為false，則即使啟用此修飾元，也不會從FXG移除它，因為需要在此路徑上繪製文字。

預設值為1。
