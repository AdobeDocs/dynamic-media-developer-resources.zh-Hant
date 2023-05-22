---
title: 設定資產
description: Carousel查看器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: e8aaee4e-56d5-46e4-8499-d5c9a6ba5d3b
source-git-commit: 96ac67e5645c2c55920cc971806ba2f14ae57044
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 4%

---

# 設定資產{#setasset}

Carousel查看器的JavaScript API參考。

` setAsset( *`asset`*)`

設定新資產。 可以在任何時間（在之前或之後）調用此參數 `init()`。 如果在 `init()`，查看器在運行時交換資產。

另請參閱 [初始化](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 資產</span> </span> </p> </td> 
   <td colname="col2"> <p>{ 0}<span class="codeph"> 字串</span>}新資產ID。 </p> <p>此查看器不支援使用IR（影像呈現）或UGC（用戶生成的內容）的影像。 </p> </td>
  </tr>
 </tbody>
</table>

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

單個影像引用：

```
<instance>.setAsset("/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner")
```

