---
description: eCatalog檢視器的JavaScript API參考。
seo-description: eCatalog檢視器的JavaScript API參考。
seo-title: setContainerId
solution: Experience Manager
title: setContainerId
topic: Dynamic media
uuid: 19149e38-b9d2-4ecd-a555-92e2960f7ee3
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# setContainerId{#setcontainerid}

eCatalog檢視器的JavaScript API參考。

[!DNL ` setContainerId( *`containerId`*)`]

設定檢視器插入的[!DNL `DOM` 容器( [!DNL `DIV`]通常為a)的ID。 您不需要在呼叫此方法時建立容器元素。 但是，容器在執行時必 [!DNL `init()`] 須存在。 必須先呼叫 [!DNL `init()`]。

如果檢視器設定資訊與 [!DNL `config`] JSON物件一起傳遞至建構函式，此方法為選用。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 容 <span class="varname"> 器ID </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}容 </span> 器的ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```

