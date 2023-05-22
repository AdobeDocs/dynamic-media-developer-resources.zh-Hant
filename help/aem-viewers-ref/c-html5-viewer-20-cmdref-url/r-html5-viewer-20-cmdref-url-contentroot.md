---
title: 內容URL
description: 所有查看器通用的參數。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: cab3c3fe-1a64-4a50-8559-57cadb31f689
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 3%

---

# 內容URL{#contenturl}

所有查看器通用的參數。

` contentUrl= *`內容Url路徑`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 內容Url路徑</span> </span> </p> </td> 
   <td colname="col2"> <p>指定自定義CSS檔案、任何隱藏字幕內容或導航內容的基本路徑。 </p> <p>如果路徑沒有前導 <span class="filepath"> /</span>，它與查看器HTML頁的位置相關。 如果路徑具有前導 <span class="filepath"> /</span>，它指定同一伺服器上的絕對路徑。 </p> <p> 不指定樣式命令時不影響預設CSS檔案的載入。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-10ee45d637134e0fbcd943c62578cb78}

選擇性.

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
