---
title: videoServerUrl
description: 智慧型裁切視訊檢視器的URL命令。
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 9bd37d2c-c7ec-4f58-8328-45c0a156f330
TQID: 'https://experienceleague.adobe.com/9OQU4jury7TJFsaZrzBQYETRKCR1N5BGbKa18HFovfQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 55
ht-degree: 5%

---

# videoServerUrl{#videoserverurl}

智慧型裁切視訊檢視器的URL命令。

` videoServerUrl= *`videoRootPath`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> videoRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p> 視訊伺服器根路徑。 若未指定網域，則改為套用伺服頁面的網域。 適用標準URI路徑解析。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選擇性. 標準SaaS使用不需要。

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

`/is/content/`

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
videoServerUrl=http://s7d1.scene7.com/is/content/
```
