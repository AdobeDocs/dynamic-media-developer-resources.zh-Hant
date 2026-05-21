---
title: ImageMapEffect.rollover
description: ImageMapEffect.rollover
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 3d5eb17d-668a-4ad8-9f84-5684941d450d
TQID: 'https://experienceleague.adobe.com/klywra9qyLFdkzwADSdRM3EvwzMJ9d2lrXSLtEViFkg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 84
ht-degree: 5%

---

# ImageMapEffect.rollover{#imagemapeffect-rollover}

`[ImageMapEffect.|<containerId>_imageMapEffect.]rollover=0|1`

<table id="table_2671D63442B54F659C32C4A3CC61DD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p>指定何時顯示資訊面板。 </p> <p>如果設為<span class="codeph"> 1</span>，則當滑鼠進入影像地圖區域時，會顯示資訊面板（如果影像地圖具有非空白的<span class="codeph"> rollover_key</span>屬性）。 </p> <p>如果設為<span class="codeph">，則在選取影像地圖時觸發了0</span>資訊面板（如果影像地圖具有非空白的<span class="codeph"> rollover_key</span>和空白的<span class="codeph"> href</span>屬性）。 </p> <p> 在觸控裝置（包括觸控式案頭系統）上忽略，並自動設為<span class="codeph"> 0</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-ccfedc2da28f412a86d03f390db92b4b}

選擇性.

## 預設 {#section-79eb39c444814c9398df1f5f3730d289}

`0`

## 範例 {#section-b548ed09b52b4b65888ac891af08d725}

`rollover=1`
