---
description: 所有檢視器通用的參數。
seo-description: 所有檢視器通用的參數。
seo-title: serverUrl
solution: Experience Manager
title: serverUrl
topic: Dynamic media
uuid: a079a223-7478-4b6a-bc99-284e3366fb30
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# serverUrl{#serverurl}

所有檢視器通用的參數。

` serverUrl= *`isRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isRootPath</span></span> </p> </td> 
   <td colname="col2"> <p>相對或絕對影像伺服根路徑。 </p> <p> 指定影像伺服的相對或絕對路徑，檢視器會從中擷取影像。 如果路徑沒有前導/ <span class="filepath"></span>，則它是相對於檢視器HTML頁面的位置。 如果路徑具有前導 <span class="filepath"> /</span>，則它指定同一伺服器上的絕對路徑。 </p> <p> 僅使用絕對路徑，以備檢視器中啟用「電子郵件共用」模組時使用。 </p> </td> 
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

