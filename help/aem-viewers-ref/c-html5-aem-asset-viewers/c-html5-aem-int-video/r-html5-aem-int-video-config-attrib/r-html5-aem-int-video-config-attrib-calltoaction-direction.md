---
title: CallToAction.direction
description: 互動式視訊檢視器的設定屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 2cfeeba0-3230-481c-857a-bed3fedc836c
TQID: 'https://experienceleague.adobe.com/YehjMoK88ylklqHA9ZpjPgW8xoMwhLQqR-2e73ayWRM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 82
ht-degree: 3%

---

# CallToAction.direction{#calltoaction-direction}

互動式視訊檢視器的設定屬性。

`[CallToAction.|<containerId>_callToAction.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">自動|靠左|靠右</span> </p> </td> 
   <td colname="col2"> <p> 指定在檢視中填入縮圖的方式。 </p> <p>設定為<span class="codeph">左</span>以設定由左至右的填入順序。 </p> <p>設定為<span class="codeph"> right </span>會反轉順序，因此檢視會以由右至左、由上到下的方向填入。 </p> <p>設定為<span class="codeph">自動</span>可在地區設定設為<span class="codeph"> "ja" </span>時，讓元件套用至右模式；否則，會使用<span class="codeph">左</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選擇性.

## 預設 {#section-71fb773f814649b2885aefee68073641}

`auto`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
direction=right
```
