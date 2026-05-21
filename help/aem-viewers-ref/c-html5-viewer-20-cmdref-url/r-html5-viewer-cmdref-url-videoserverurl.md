---
title: videoServerUrl
description: 所有檢視器通用的引數。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: db0ce8c4-3754-4fef-9430-44ee8e5c5e80
TQID: 'https://experienceleague.adobe.com/rHcYe13DDclS1Y7rguOHBuAGP-IH9oxzqpp7uorHc2Y'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 63
ht-degree: 4%

---

# videoServerUrl{#videoserverurl}

所有檢視器通用的引數。

>[!NOTE]
>
>這個命令不適用於Video Image Viewer。

` videoServerUrl= *`videoRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> videoRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p> 視訊伺服器根路徑。 若未指定網域，則改為套用伺服頁面的網域。 適用標準URI路徑解析。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-10ee45d637134e0fbcd943c62578cb78}

選擇性. 標準軟體即服務使用不需要。

## 預設 {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/content/`

## 範例 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
videoServerUrl=http://s7d1.scene7.com/is/content/
```
