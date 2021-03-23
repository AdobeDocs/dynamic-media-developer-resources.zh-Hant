---
description: 不透明度. 指定材質不透明度。
seo-description: 不透明度. 指定材質不透明度。
seo-title: opac
solution: Experience Manager
title: opac
uuid: 0f5b11f0-af65-4abd-947e-7a28cb8de263
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 4%

---


# opac{#opac}

不透明度. 指定材質不透明度。

` opac= *`val`*`

<table id="simpletable_6AB8CD75F526469FBC9FEAE049792EF2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>材料不透明度（百分比）;0...100 </p> </td> 
 </tr> 
</table>

下列材質／物件組合支援可變的不透明度：

* 套用至可文字化重疊物件的純色和可重複紋理。
* 應用於窗口覆蓋框架對象的窗口覆蓋材料。
* 貼文套用至可文字化物件或牆狀物件。

如果材料包括具有Alpha通道的影像，則`opac=`可用於使影像更透明，但不是更不透明。

## 屬性 {#section-352f7b82ede54159b6afb90ae4b559ec}

材料屬性。 如果當前對象選擇或材料不支援不透明度，則忽略。

## 預設 {#section-bd45105b1e614f96ad5d521e3ef65736}

`opac=100`，對於完全不透明的材料（如果影像不包括alpha通道）。
