---
title: setAsset
description: 影片影像檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: e5f88bc9-a880-45eb-9554-57e185937d29
TQID: 'https://experienceleague.adobe.com/s0cxnymzd8SKbvW5DwOY8i6XpwWofN5hkDbv-BTPXE0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 76
ht-degree: 2%

---

# setAsset{#setasset}

影片影像檢視器的JavaScript API參考。

` setAsset( *`資產`*)`

設定新資產。 您可以隨時在`init()`之前或之後呼叫此引數。 如果在`init()`之後呼叫，檢視器會在執行階段交換資產。

另請參閱[init](../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-javascriptapiref/r-html5-aem-int-image-viewer-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">資產</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph">字串</span>}新資產識別碼。 </p> <p>此檢視器不支援使用IR （影像演算）或UGC （使用者產生的內容）的影像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

單一影像參考：

```
<instance>.setAsset("/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg")
```
