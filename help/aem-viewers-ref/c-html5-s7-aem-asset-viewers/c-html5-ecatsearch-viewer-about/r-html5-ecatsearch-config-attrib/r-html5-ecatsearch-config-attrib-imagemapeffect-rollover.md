---
description: ImageMapEffect.rollover
solution: Experience Manager
title: ImageMapEffect.rollover
topic: Dynamic media
uuid: 276122d8-2109-42eb-be13-bead35cd3fe2
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
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
   <td colname="col2"> <p>指定何時顯示資訊面板。 </p> <p>如果設為<span class="codeph"> 1</span>，則當滑鼠進入影像地圖區域時會顯示資訊面板（若影像地圖具有非空白的<span class="codeph"> rolver_key</span>屬性）。 </p> <p>如果設為<span class="codeph"> 0</span>資訊面板會在點按影像地圖時觸發（如果影像地圖具有非空白的<span class="codeph"> rolver_key</span>和空白的<span class="codeph"> href</span>屬性）。 </p> <p> 在觸控裝置（包括可觸控的案頭系統）上忽略，並自動設為<span class="codeph"> 0</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-ccfedc2da28f412a86d03f390db92b4b}

選填。

## 預設 {#section-79eb39c444814c9398df1f5f3730d289}

[!DNL `0`]

## 範例 {#section-b548ed09b52b4b65888ac891af08d725}

[!DNL `rollover=1`]
