---
title: ImageMapEffect.rollover
description: ImageMapEffect.rollover
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 3d5eb17d-668a-4ad8-9f84-5684941d450d
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 5%

---

# ImageMapEffect.rollover{#imagemapeffect-rollover}

`[ImageMapEffect.|<containerId>_imageMapEffect.]rollover=0|1`

<table id="table_2671D63442B54F659C32C4A3CC61DD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p>指定何時顯示資訊面板。 </p> <p>如果設定為 <span class="codeph"> 1</span>，當滑鼠進入影像映射區時，將顯示資訊面板(如果影像映射為非空， <span class="codeph"> rovel_key</span> 屬性)。 </p> <p>如果設定為 <span class="codeph"> 0</span> 選擇影像映射時(如果影像映射具有非空的 <span class="codeph"> rovel_key</span> 空 <span class="codeph"> href</span> 屬性)。 </p> <p> 在觸摸設備（包括啟用觸摸的台式機系統）上忽略，並自動設定為 <span class="codeph"> 0</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-ccfedc2da28f412a86d03f390db92b4b}

選擇性.

## 預設 {#section-79eb39c444814c9398df1f5f3730d289}

`0`

## 範例 {#section-b548ed09b52b4b65888ac891af08d725}

`rollover=1`
