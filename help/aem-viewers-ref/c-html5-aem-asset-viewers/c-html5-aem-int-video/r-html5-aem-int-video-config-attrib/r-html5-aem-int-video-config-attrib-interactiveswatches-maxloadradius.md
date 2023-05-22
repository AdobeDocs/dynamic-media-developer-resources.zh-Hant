---
title: InteractiveSwatches.maxloadradius
description: Interactive Video Viewer的配置屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 16c9c70a-352d-4a21-bb14-2f9e266a83e8
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 4%

---

# InteractiveSwatches.maxloadradius{#interactiveswatches-maxloadradius}

Interactive Video Viewer的配置屬性。

` [InteractiveSwatches.|<containerId>_interactiveSwatches.]maxloadradius=-1|0| *`預載入br`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">1|0|<span class="varname"> 預載入br</span></span> </p> </td> 
   <td colname="col2"> <p> 指定元件預載入行為。 </p> <p>設定為時 <span class="codeph"> -1</span> 初始化元件或更改資產時，將同時載入所有色板。 </p> <p>設定為時 <span class="codeph"> 0</span> 只載入可見色板。 </p> <p>設定為 <span class="codeph"><span class="varname"> 預載入br</span></span> 定義在可見區域周圍預載入的不可見行/列數。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選擇性.

## 預設 {#section-71fb773f814649b2885aefee68073641}

`1`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
maxloadradius=-1
```
