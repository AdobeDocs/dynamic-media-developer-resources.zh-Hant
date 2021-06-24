---
description: 互動式視訊檢視器的設定屬性。
solution: Experience Manager
title: CallToAction.fmt
feature: Dynamic Media Classic，檢視器， SDK/API，互動式影片
role: Developer,Business Practitioner
exl-id: 38ca592f-329c-4fd4-8dbc-a49000663e55
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 5%

---

# CallToAction.fmt{#calltoaction-fmt}

互動式視訊檢視器的設定屬性。

`[CallToAction.|<containerId>_callToAction.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif|alpha</span> </p> </td> 
   <td colname="col2"> <p> 指定元件用於從影像伺服器載入影像的影像格式。 </p> <p>如果指定的格式結尾為「<span class="codeph"> -alpha</span>」，則元件會將影像呈現為透明內容。 對於所有其他影像格式，元件將影像視為不透明。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選填。

## 預設 {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
fmt=png-alpha
```
