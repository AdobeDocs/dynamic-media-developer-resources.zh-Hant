---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.preloadtiles
solution: Experience Manager
title: FlyoutZoomView.preloadtiles
topic: Dynamic media
uuid: c9989916-d0f3-4268-932a-e12c693f5b74
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 7%

---


# FlyoutZoomView.preloadtiles{#flyoutzoomview-preloadtiles}

`[FlyoutZoomView.|<containerId>_flyout.]preloadtiles=0|1`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 設為<span class="codeph"> 1</span>以啟用縮放影像的預先載入。 </p> <p>設為<span class="codeph"> 0</span>，視需要遞增載入縮放影像。 </p> <p> <p>注意： 請注意，如果您啟用此選項，可能會導致頻寬使用率大幅提高，因為縮放後的影像必須完整載入，即使使用者未執行縮放動作亦然。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preloadtiles=1`
