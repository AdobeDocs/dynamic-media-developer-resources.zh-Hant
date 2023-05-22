---
title: CallToAction.maxloadradius
description: Interactive Video Viewer的配置屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: db04133e-bb23-4d94-b91d-fcf34576c03f
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 4%

---

# CallToAction.maxloadradius{#calltoaction-maxloadradius}

Interactive Video Viewer的配置屬性。

` [CallToAction.|<containerId>_callToAction.]maxloadradius=-1|0| *`預載入br`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-1|0|<span class="varname"> 預載入br</span></span> </p> </td> 
   <td colname="col2"> <p> 指定元件預載入行為。 </p> <p>設定為時 <span class="codeph"> -1</span> 初始化元件或更改資產時，將同時載入所有縮略圖。 </p> <p>設定為時 <span class="codeph"> 0</span> 只載入可見的縮略圖。 </p> <p>設定為 <span class="codeph"><span class="varname"> 預載入br</span></span> 定義在可見區域周圍預載入的不可見行/列數。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選擇性.

## 預設 {#section-71fb773f814649b2885aefee68073641}

`-1`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
maxloadradius=-1
```
