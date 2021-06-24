---
description: 所有檢視器通用的參數。
solution: Experience Manager
title: serverUrl
feature: Dynamic Media Classic，檢視器，SDK/API
role: Developer,Business Practitioner
exl-id: c9da3d5b-492d-4e1f-8fdc-3255b2b40fc6
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 3%

---

# serverUrl{#serverurl}

所有檢視器通用的參數。

` serverUrl= *`isRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p>相對或絕對影像伺服根路徑。 </p> <p> 指定「影像伺服」的相對或絕對路徑，檢視器會從該處擷取影像。 如果路徑的前導字元為<span class="filepath"> /</span>，則會相對於檢視器HTML頁面的位置。 如果路徑的前導<span class="filepath"> /</span> ，則它指定同一伺服器上的絕對路徑。 </p> <p> 若檢視器中已啟用電子郵件共用模組，請僅使用絕對路徑。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-10ee45d637134e0fbcd943c62578cb78}

選填。標準SaaS（軟體即服務）使用不需要。

## 預設 {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/image/`

## 範例 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
serverUrl=http://s7d9.scene7.com/is/image/
```

```
serverUrl=http://aodmarketingna.assetsadobe.com/is/image
```

```
serverUrl=https://adobedemo62-h.assetsadobe.com/is/image
```
