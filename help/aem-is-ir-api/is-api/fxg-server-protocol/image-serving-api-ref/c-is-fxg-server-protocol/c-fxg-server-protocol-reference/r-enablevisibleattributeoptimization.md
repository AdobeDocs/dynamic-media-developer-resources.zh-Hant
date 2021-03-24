---
description: 啟用FXG的優化。
solution: Experience Manager
title: enableVisibleAttributeOptimization
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 2%

---


# enableVisibleAttributeOptimization{#enablevisibleattributeoptimization}

啟用FXG的優化。

<table id="simpletable_FDE0D8786BC747AF87A336452500E695"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> enableVisibleAttributeOptimization(&amp;E)</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

移除在FXG中其可見度設為false的元素，同時傳遞此FXG，進而減少FXG的處理時間。 雖然它只會移除可見度為false且不會影響FXG中任何其他元素的元素。 例如，如果`Path`上有文字，而`Path`的可見度設為false，則即使啟用此修飾詞，也不會從FXG移除它，因為文字需要在此路徑上繪製。

預設為 1。
