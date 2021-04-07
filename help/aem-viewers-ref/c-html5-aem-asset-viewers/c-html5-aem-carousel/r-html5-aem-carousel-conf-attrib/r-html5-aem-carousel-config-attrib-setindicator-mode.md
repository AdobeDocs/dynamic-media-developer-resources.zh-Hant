---
description: SetIndicator.mode
solution: Experience Manager
title: SetIndicator.mode
feature: Dynamic Media經典，檢視器，SDK/API，轉盤橫幅
role: 開發人員，商業從業人員
exl-id: f228cf05-8b74-4f85-a02e-3bc084581529
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 5%

---

# SetIndicator.mode{#setindicator-mode}

`[SetIndicator.|<containerId>_setIndicator.]mode=numeric|dotted`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 數值|點數</span> </p> </td> 
   <td colname="col2"> <p> 配置設定指示符的渲染樣式。 </p> <p>當設為<span class="codeph"> dotted</span>時，元件會為所有頁面呈現相同的指示符。 </p> <p>設為<span class="codeph"> numeric</span>時，會在每個指標元素中放置一個以1為基礎的頁碼。 </p> <p>能夠觸摸輸入的設備不支援<span class="codeph">數字</span>操作模式。 而是在此類裝置上使用<span class="codeph"> dotted</span>元件。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選填。

## 預設 {#section-71fb773f814649b2885aefee68073641}

`dotted`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`mode=numeric`
