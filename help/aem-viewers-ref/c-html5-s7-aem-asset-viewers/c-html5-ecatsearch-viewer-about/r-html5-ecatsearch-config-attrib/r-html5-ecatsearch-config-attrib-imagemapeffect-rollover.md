---
description: ImageMapEffect.rollover
solution: Experience Manager
title: ImageMapEffect.rollover
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog搜尋
role: Developer,User
exl-id: 29ca3d4d-6953-4148-9b1e-01e94d1da7df
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 5%

---

# ImageMapEffect.rollover{#imagemapeffect-rollover}

[!DNL `[ImageMapEffect.|<containerId>_imageMapEffect.]rollover=0|1`]

<table id="table_2671D63442B54F659C32C4A3CC61DD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p>指定何時顯示資訊面板。 </p> <p>如果設為<span class="codeph"> 1</span>，則當滑鼠進入影像映射區域時，將顯示資訊面板（如果影像映射具有非空的<span class="codeph"> rovelp_key</span>屬性）。 </p> <p>如果設為<span class="codeph"> 0</span>資訊面板是在點按影像映射時觸發的（如果影像映射具有非空<span class="codeph">變換鍵</span>和空<span class="codeph"> href</span>屬性）。 </p> <p> 在觸控式裝置上忽略，包括觸控式案頭系統，且會自動設為<span class="codeph"> 0</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-ccfedc2da28f412a86d03f390db92b4b}

選填。

## 預設 {#section-79eb39c444814c9398df1f5f3730d289}

[!DNL `0`]

## 範例 {#section-b548ed09b52b4b65888ac891af08d725}

[!DNL `rollover=1`]
