---
title: setParam
description: 轉盤檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 0829933f-a90b-4066-9904-748f2a727169
TQID: 'https://experienceleague.adobe.com/BB5asMbiHW7HFp57O91IhhVNaqJAPG9kxzb6hal-oHY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 83
ht-degree: 3%

---

# setParam{#setparam}

轉盤檢視器的JavaScript API參考。

` setParam( *`名稱，值`*)`

將檢視器引數設定為指定的值。 引數是檢視器特定的組態選項或軟體開發套件修飾元。 在`init()`之前呼叫此引數。

如果檢視器組態資訊已與`config` JSON物件一併傳遞給建構函式，則此方法為選用。

另請參閱[xref](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md)。

## 參數 {#section-c68a5a3688d342fd9d6a7fd59867cc7a}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">名稱</span> </span> </p> </td>
   <td colname="col2"> <p> <span class="codeph"> {string}引數的</span>名稱。 </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">值</span> </span> </p> </td>
   <td colname="col2"> <p> <span class="codeph"> {string}引數的</span>值。 值不得以百分比編碼。 </p> </td>
  </tr>
 </tbody>
</table>

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "etc/dam/presets/css/html5_carouselviewer_dotted_light.css")
```
