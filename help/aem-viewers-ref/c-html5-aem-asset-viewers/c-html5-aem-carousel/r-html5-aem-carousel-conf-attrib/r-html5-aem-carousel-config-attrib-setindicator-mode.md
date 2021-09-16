---
title: SetIndicator.mode
description: SetIndicator.mode
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: f228cf05-8b74-4f85-a02e-3bc084581529
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 6%

---

# SetIndicator.mode{#setindicator-mode}

`[SetIndicator.|<containerId>_setIndicator.]mode=numeric|dotted`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 數值|虛點</span> </p> </td> 
   <td colname="col2"> <p> 配置設定指示符的呈現樣式。 </p> <p>當設為<span class="codeph">虛線</span>時，元件會為所有頁面呈現相同的指標。 </p> <p>設為<span class="codeph"> numeric</span>時，會在每個指標元素內放入以1為基礎的頁碼。 </p> <p>具有觸控輸入的裝置不支援<span class="codeph">數值</span>操作模式。 元件會改為在這類裝置上使用<span class="codeph">虛線</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選填。

## 預設 {#section-71fb773f814649b2885aefee68073641}

`dotted`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`mode=numeric`
