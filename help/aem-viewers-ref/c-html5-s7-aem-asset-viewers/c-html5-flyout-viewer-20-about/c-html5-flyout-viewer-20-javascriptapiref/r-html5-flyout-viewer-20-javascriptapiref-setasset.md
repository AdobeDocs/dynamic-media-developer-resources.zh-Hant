---
description: 飛出檢視器的JavaScript API參考。
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic，檢視器，SDK/API,Flyout
role: Developer,Business Practitioner
exl-id: cd66267e-7b25-4af4-b83c-f7b7f768ea8c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 2%

---

# setAsset{#setasset}

飛出檢視器的JavaScript API參考。

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 資產</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph">字串</span>}新資產ID、顯式影像集或顯式影像集，具有幀特定的影像伺服修飾元，並在<span class="codeph"> ?</span>後附加可選的全局影像伺服修飾元。 </p> <p> 此檢視器不支援使用IR（影像轉譯）或UGC（使用者產生的內容）的影像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

設定新資產。 您可以在`init()`之前或之後隨時呼叫此參數。 如果在`init()`之後呼叫，檢視器會在執行階段交換資產。

另請參閱[init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463)。

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

單一影像參考：

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

對目錄中定義的影像集的單個引用：

```
<instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample")
```

顯式影像集：

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C")
```

使用特定於幀的影像伺服修飾元設定的顯式影像集：

```
<instance>.setAsset("(Scene7SharedAssets/Backpack_B?op_colorize=255%2C0%2C0,Scene7SharedAssets/Backpack_B?op_colorize=0x00ff00)")
```

集合中的所有影像都新增銳利化修飾元：

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C?op_sharpen=1")
```
