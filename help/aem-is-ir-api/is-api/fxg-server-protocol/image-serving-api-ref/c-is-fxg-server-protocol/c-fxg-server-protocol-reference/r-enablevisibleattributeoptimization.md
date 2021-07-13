---
description: 實現FXG的優化。
solution: Experience Manager
title: enableVisibleAttributeOptimization
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a643694e-f6a2-424e-8f6e-3dbb4cdc41b3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 3%

---

# enableVisibleAttributeOptimization{#enablevisibleattributeoptimization}

實現FXG的優化。

<table id="simpletable_FDE0D8786BC747AF87A336452500E695"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> enableVisibleAttributeOptimization(&amp;E)</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

在傳遞此FXG時，移除其可見性在FXG中設為false的元素，而這進而減少FXG的處理時間。 儘管它僅會移除可見度為false的元素，而不會影響FXG中的任何其他元素。 例如，如果`Path`上有文本，且`Path`的可見性設定為false，則即使啟用此修飾符，也不會從FXG中刪除該文本，因為需要在此路徑上繪製文本。

預設為 1。
