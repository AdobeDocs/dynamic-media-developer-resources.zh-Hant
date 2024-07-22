---
title: SpinView.enableHD
description: SpinView.enableHD
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0a2abdc6-eae5-4dda-b749-599cd8a07a98
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 3%

---

# SpinView.enableHD{#spinview-enablehd}

` [SpinView.|<containerId>_spinView.]enableHD=always|never|limit[, *`數字`*]`

<table id="table_8929B59833DE4E1C89FA4BCF07309809"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">一律|永不|限制</span> </p> </td> 
   <td colname="col2"> <p> 啟用、限制或停用<span class="codeph"> devicePixelRatio</span>大於<span class="codeph"> 1</span>之裝置的最佳化功能，亦即配備高密度顯示器的裝置(如iPhone4和類似裝置)。 如果啟用，則元件會限制IS影像要求的大小，彷彿裝置的畫素比僅有<span class="codeph"> 1</span>，因此會減少頻寬。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname">數字</span></span> </p> </td> 
   <td colname="col2"> <p> 如果使用<span class="codeph">限制</span>設定，元件僅啟用指定上限的高畫素密度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選擇性.

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`limit,1500`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`enableHD=always`
