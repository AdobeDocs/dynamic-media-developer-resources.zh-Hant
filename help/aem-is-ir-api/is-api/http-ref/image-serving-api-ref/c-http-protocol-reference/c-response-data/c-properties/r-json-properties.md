---
description: 如果將jsonp指定為回應格式，則回覆資料會使用JSONP（含邊框間距的JavaScript物件標籤法）格式化，並包裝在JavaScript函式呼叫中。
solution: Experience Manager
title: JSONP屬性
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 2294eb37-b362-438f-94bc-eb24ca641752
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 1%

---

# JSONP屬性{#jsonp-properties}

如果將jsonp指定為回應格式，則回覆資料會使用JSONP（含邊框間距的JavaScript物件標籤法）格式化，並包裝在JavaScript函式呼叫中。

客戶端可指定可選的唯一請求標識符(*`reqId`*)，該標識符在響應中返回，並允許客戶端區分非同步接收的多個響應。 典型回應的一般結構如下：

```
/*jsonp*/s7jsonResponse({ 
   " 
<varname>
  objectName 
</varname>. 
<varname>
  propertyName 
</varname>" : " 
<varname>
  propertyValue 
</varname>", 
   ... 
 }, " 
<varname>
  reqId 
</varname>" );
```

`s7jsonResponse` JavaScript函式必須由用戶端定義。 在最簡單的形式中，函式可能如下所示：

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

支援JSONP回應格式的要求可讓您使用`req=`參數的延伸語法來指定JS回呼處理常式的名稱：

`req=...,json [&handler = reqHandler]`

`<reqHandler>` 是JSONP回應中出現的JS處理常式的名稱。僅允許a-z、A-Z和0-9個字元。 選填。預設為 `s7jsonResponse`.

Dynamic Media影像伺服檢視器套件包含公用程式，可從影像伺服中要求和剖析JSONP格式化資料。

如需JSONP格式的詳細資訊，請參閱[http://en.wikipedia.org/wiki/JSONP](http://en.wikipedia.org/wiki/JSONP)。

如需JSON格式的詳細資訊，請參閱[www.json.org](http://www.json.org)。

另請參閱[req](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)。
