---
title: serverUrl
description: 所有檢視器通用的引數。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: c9da3d5b-492d-4e1f-8fdc-3255b2b40fc6
source-git-commit: ce1ac4938c7baf482c6c55a9ad13379153a3ec5b
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 2%

---

# serverUrl{#serverurl}

所有檢視器通用的引數。

` serverUrl= *`isRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p>相對或絕對的「影像伺服」根路徑。 </p> <p> 指定「影像伺服」的相對或絕對路徑，檢視器可從中擷取影像。 如果路徑沒有前導的<span class="filepath"> /</span>，則為檢視器HTML頁面的相對位置。 如果路徑的前導為<span class="filepath"> /</span>，它會在相同伺服器上指定絕對路徑。 </p> <p> 在檢視器中啟用電子郵件共用模組時，僅使用絕對路徑。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-10ee45d637134e0fbcd943c62578cb78}

選填。 標準SaaS （軟體即服務）使用不需要。

## 預設 {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/image/`

## 範例 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
serverUrl=http://s7d9.scene7.com/is/image/
```

```
serverUrl=http://aodmarketingna.assetsadobe.com/is/image
```

<!--

```
serverUrl=https://adobedemo62-h.assetsadobe.com/is/image
```

-->
