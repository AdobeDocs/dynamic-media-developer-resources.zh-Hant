---
description: 所有檢視器通用的參數。
seo-description: 所有檢視器通用的參數。
seo-title: contentUrl
solution: Experience Manager
title: contentUrl
topic: Dynamic media
uuid: 85b00c4e-b382-4970-b780-e4ef59108cb7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# contentUrl{#contenturl}

所有檢視器通用的參數。

` contentUrl= *`contentUrlPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> contentUrlPath <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p>指定自訂CSS檔案、任何隱藏字幕內容或導覽內容的基本路徑。 </p> <p>如果路徑沒有前導/ <span class="filepath"></span>，則它是相對於檢視器HTML頁面的位置。 如果路徑具有前導 <span class="filepath"> /</span>，則它指定同一伺服器上的絕對路徑。 </p> <p> 不指定樣式命令時，不會影響預設CSS檔案的載入。 </p> </td> 
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

