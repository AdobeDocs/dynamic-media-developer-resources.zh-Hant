---
description: SetIndicator.mode
solution: Experience Manager
title: SetIndicator.mode
topic: Dynamic media
uuid: cfb549c2-e0cf-46c3-b5b7-219c8c1bee94
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 6%

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
