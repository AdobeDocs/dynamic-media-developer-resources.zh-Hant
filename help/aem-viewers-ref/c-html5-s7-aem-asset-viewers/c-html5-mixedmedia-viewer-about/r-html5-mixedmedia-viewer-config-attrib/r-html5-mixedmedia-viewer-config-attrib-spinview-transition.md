---
description: SpinView.transition
solution: Experience Manager
title: SpinView.transition
feature: Dynamic Media Classic，檢視器，SDK/API，混合媒體集
role: Developer,Business Practitioner
exl-id: fcffe282-65a5-4093-8838-71a64085b387
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 4%

---

# SpinView.transition{#spinview-transition}

` [SpinView.|<containerId>_spinView.]transition= *``*[, *`調整`*]`

<table id="table_5B8094216AE94DC59671E06DB941A366"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 時間</span></span> </p> </td> 
   <td colname="col2"> <p> 指定單縮放步驟操作的動畫所花費的秒數。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 寬鬆</span></span> </p> </td> 
   <td colname="col2"> <p> 建立加速或減速的假象，使轉變更自然。 您可以將緩動設為下列其中一個項目： </p> <p> 
     <ul id="ul_7B9694978D96449AB986AED1CF7F649D"> 
      <li id="li_904CEC8AD5834139A5585EE70ACE9C80">0（自動） </li> 
      <li id="li_471D4CD39C10415497B1714B0AD961B9"> 1（線性） </li> 
      <li id="li_7A0F9F1186604E75BAA19626A844236A"> 2（二次） </li> 
      <li id="li_B8D4C40D795642AB835925582B707158"> 3（立方） </li> 
      <li id="li_2B9F7324BB89455C89C1CAE1BD5BBB65"> 4（四分位） </li> 
      <li id="li_B94A553B6E844247BE88ECA0A8CEB811"> 5（五次） </li> 
     </ul> </p> <p>停用彈性縮放時（預設值），「自動」模式一律使用線性轉變。 否則，它適合基於轉變時間的其他緩動功能之一。 即，過渡時間越短，加速或減速效果的加緩函式就越大。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0.5,0`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=2,2`
