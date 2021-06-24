---
description: 檢視器會在主檢視上顯示搜尋結果區域，以反白標示在目錄中找到的字詞或片語。
solution: Experience Manager
title: 搜尋效果
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog搜尋
role: Developer,Business Practitioner
exl-id: 3591edb0-4b0a-4761-af87-c372132c5138
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 1%

---

# 搜尋效果{#search-effect}

檢視器會在主檢視上顯示搜尋結果區域，以反白標示在目錄中找到的字詞或片語。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主查看器區域的CSS屬性**

搜索結果區域的外觀由以下CSS類選擇器控制：

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
   <td colname="col2"> <p>搜索結果區域的背景。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要使用半透明的黃色填充設定搜索結果區域：

```
.s7ecatalogsearchviewer .s7searcheffect .s7region { 
 background: rgba(255,255,0, 0.5); 
}
```
