---
title: 伺服器URL
description: 所有查看器通用的參數。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: c9da3d5b-492d-4e1f-8fdc-3255b2b40fc6
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 3%

---

# 伺服器URL{#serverurl}

所有查看器通用的參數。

` serverUrl= *`是根路徑`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 是根路徑</span> </span> </p> </td> 
   <td colname="col2"> <p>相對或絕對影像服務根路徑。 </p> <p> 指定影像服務的相對或絕對路徑，查看器從中檢索影像。 如果路徑沒有前導 <span class="filepath"> /</span>，它與查看器HTML頁的位置相關。 如果路徑具有前導 <span class="filepath"> /</span>，它指定同一伺服器上的絕對路徑。 </p> <p> 如果在查看器中啟用了電子郵件共用模組，則只使用絕對路徑。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-10ee45d637134e0fbcd943c62578cb78}

選擇性. 標準SaaS（軟體即服務）使用不需要。

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
