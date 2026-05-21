---
title: setAsset
description: 內嵌縮放檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 62b46ad5-90b7-49e1-a426-87fbe956f07e
TQID: 'https://experienceleague.adobe.com/-25X3APJGqrlx1F5awqzGpfSsyKBjw7xpHYMvbgqS2I'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 130
ht-degree: 1%

---

# setAsset{#setasset}

內嵌縮放檢視器的JavaScript API參考。

` setAsset( *`資產`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">資產</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>}新資產ID、明確影像集或明確影像集，具有影格特定的「影像伺服」修飾元，並在<span class="codeph"> ？</span>後附加選用的全域「影像伺服」修飾元。 </p> <p> 此檢視器不支援使用IR （影像演算）或UGC （使用者產生的內容）的影像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

設定新資產。 您可以隨時在`init()`之前或之後呼叫此引數。 如果在`init()`之後呼叫，檢視器會在執行階段交換資產。

另請參閱[init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463)。

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

單一影像參考：

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

目錄中所定義影像集的單一參照：

```
<instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample")
```

明確的影像集：

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C")
```

使用影格特定的「影像伺服」修飾元的明確影像集：

```
<instance>.setAsset("(Scene7SharedAssets/Backpack_B?op_colorize=255%2C0%2C0,Scene7SharedAssets/Backpack_B?op_colorize=0x00ff00)")
```

銳利化修飾元已新增至集中的所有影像：

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C?op_sharpen=1")
```
