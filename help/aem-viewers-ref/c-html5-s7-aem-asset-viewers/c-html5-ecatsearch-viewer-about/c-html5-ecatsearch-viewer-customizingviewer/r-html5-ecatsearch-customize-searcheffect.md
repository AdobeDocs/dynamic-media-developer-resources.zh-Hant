---
description: 檢視器會在主檢視上方顯示搜尋結果區域，以反白標示在目錄中找到的字詞或片語。
solution: Experience Manager
title: 搜尋效果
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 1%

---


# 搜尋效果{#search-effect}

檢視器會在主檢視上方顯示搜尋結果區域，以反白標示在目錄中找到的字詞或片語。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主檢視器區域的CSS屬性**

使用下列CSS類別選擇器來控制搜尋結果區域的外觀：

`.s7ecatalogsearchviewer .s7searcheffect .s7region`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景  </span> </p> </td> 
   <td colname="col2"> <p>搜尋結果區域的背景。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——要使用半透明的黃色填充設定搜索結果區域：

```
.s7ecatalogsearchviewer .s7searcheffect .s7region { 
 background: rgba(255,255,0, 0.5); 
}
```

