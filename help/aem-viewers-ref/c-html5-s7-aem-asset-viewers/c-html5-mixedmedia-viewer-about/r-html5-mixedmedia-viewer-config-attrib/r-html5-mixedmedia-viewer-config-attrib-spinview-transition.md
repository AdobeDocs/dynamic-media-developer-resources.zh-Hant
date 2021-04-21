---
description: SpinView.transition
solution: Experience Manager
title: SpinView.transition
feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 4%

---


# SpinView.transition{#spinview-transition}

` [SpinView.|<containerId>_spinView.]transition= *`調`*[, *`整`*]`

<table id="table_5B8094216AE94DC59671E06DB941A366"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 時間</span></span> </p> </td> 
   <td colname="col2"> <p> 指定單一縮放步驟動作的動畫所花的時間（以秒為單位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 寬鬆</span></span> </p> </td> 
   <td colname="col2"> <p> 產生加速或減速的錯覺，使轉場更自然。 您可以將加減速設定為以下任一選項： </p> <p> 
     <ul id="ul_7B9694978D96449AB986AED1CF7F649D"> 
      <li id="li_904CEC8AD5834139A5585EE70ACE9C80">0（自動） </li> 
      <li id="li_471D4CD39C10415497B1714B0AD961B9"> 1（線性） </li> 
      <li id="li_7A0F9F1186604E75BAA19626A844236A"> 2（二次） </li> 
      <li id="li_B8D4C40D795642AB835925582B707158"> 3（立方） </li> 
      <li id="li_2B9F7324BB89455C89C1CAE1BD5BBB65"> 4（四分位） </li> 
      <li id="li_B94A553B6E844247BE88ECA0A8CEB811"> 5（五分） </li> 
     </ul> </p> <p>在停用彈性縮放時，自動模式一律會使用線性轉場（預設）。 否則，它適合基於過渡時間的其它一種緩動功能。 即，過渡時間越短，加減速作用越強。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0.5,0`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=2,2`
