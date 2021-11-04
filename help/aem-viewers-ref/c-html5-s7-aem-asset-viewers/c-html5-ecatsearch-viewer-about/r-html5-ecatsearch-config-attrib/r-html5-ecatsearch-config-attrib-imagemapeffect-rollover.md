---
description: ImageMapEffect.rollover
solution: Experience Manager
title: ImageMapEffect.rollover
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 29ca3d4d-6953-4148-9b1e-01e94d1da7df
source-git-commit: fd3a1fe47da5ba26b53ea9414bfec1e4c11d7392
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 6%

---

# ImageMapEffect.rollover{#imagemapeffect-rollover}

[!DNL `[ImageMapEffect.|<containerId>_imageMapEffect.]rollover=0|1`]

<table id="table_2671D63442B54F659C32C4A3CC61DD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p>指定何時顯示資訊面板。 </p> <p>若設為 <span class="codeph"> 1</span>，則當滑鼠進入影像映射區域時，會顯示資訊面板(如果影像映射為非空白，則 <span class="codeph"> rovell_key</span> 屬性)。 </p> <p>若設為 <span class="codeph"> 0</span> 選取影像對應時(如果影像對應具有非空白的 <span class="codeph"> rovell_key</span> 空白 <span class="codeph"> href</span> 屬性)。 </p> <p> 在觸控式裝置上忽略，包括可觸控的案頭系統，且會自動設為 <span class="codeph"> 0</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-ccfedc2da28f412a86d03f390db92b4b}

選填。

## 預設 {#section-79eb39c444814c9398df1f5f3730d289}

[!DNL `0`]

## 範例 {#section-b548ed09b52b4b65888ac891af08d725}

[!DNL `rollover=1`]
