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
ht-degree: 4%

---

# SetIndicator.mode{#setindicator-mode}

`[SetIndicator.|<containerId>_setIndicator.]mode=numeric|dotted`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 數字|虛點</span> </p> </td> 
   <td colname="col2"> <p> 配置設定指示器的渲染樣式。 </p> <p>設定為時 <span class="codeph"> 虛 </span>，該元件為所有頁面呈現相同的指示符。 </p> <p>設定為時 <span class="codeph"> 數字</span> 它在每個指示符元素內放置一個基於1的頁碼。 </p> <p>的 <span class="codeph"> 數字</span> 具有觸摸輸入的設備不支援操作模式。 相反，元件使用 <span class="codeph"> 虛</span> 在這些設備上。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選擇性.

## 預設 {#section-71fb773f814649b2885aefee68073641}

`dotted`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`mode=numeric`
