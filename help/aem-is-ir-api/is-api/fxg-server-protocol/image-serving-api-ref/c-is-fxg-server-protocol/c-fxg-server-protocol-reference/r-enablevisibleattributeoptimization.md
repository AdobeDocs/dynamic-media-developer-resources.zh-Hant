---
description: 啟用FXG的優化。
solution: Experience Manager
title: enableVisibleAttributeOptimization
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a643694e-f6a2-424e-8f6e-3dbb4cdc41b3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 3%

---

# enableVisibleAttributeOptimization{#enablevisibleattributeoptimization}

啟用FXG的優化。

<table id="simpletable_FDE0D8786BC747AF87A336452500E695"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &amp;enableVisibleAttributeOptimization</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

在傳遞此FXG時刪除其可見性在FXG中設定為false的元素，這進而減少了FXG的處理時間。 儘管它只刪除那些可視性為false且不會影響FXG中任何其他元素的元素。 例如，如果上有文本 `Path` 和能見度 `Path` 設定為false，則即使啟用了此修飾符，也不會從FXG中刪除它，因為需要在此路徑上繪製文本。

預設為 1。
