---
description: 所有檢視器通用的參數。
solution: Experience Manager
title: contentUrl
feature: Dynamic Media Classic，檢視器，SDK/API
role: Developer,User
exl-id: cab3c3fe-1a64-4a50-8559-57cadb31f689
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 4%

---

# contentUrl{#contenturl}

所有檢視器通用的參數。

` contentUrl= *`contentUrlPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> contentUrlPath</span> </span> </p> </td> 
   <td colname="col2"> <p>指定自訂CSS檔案、任何隱藏式字幕內容或導覽內容的基本路徑。 </p> <p>如果路徑的前導字元為<span class="filepath"> /</span>，則會相對於檢視器HTML頁面的位置。 如果路徑的前導<span class="filepath"> /</span> ，則它指定同一伺服器上的絕對路徑。 </p> <p> 不指定style命令時，不會影響預設CSS檔案的載入。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-10ee45d637134e0fbcd943c62578cb78}

選填。

## 預設 {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/content/`

## 範例 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
contentUrl=/skins/
```

```
contentUrl=http://aodmarketingna.assetsadobe.com/
```

```
contentUrl=https://demos-pub.assetsadobe.com/
```
