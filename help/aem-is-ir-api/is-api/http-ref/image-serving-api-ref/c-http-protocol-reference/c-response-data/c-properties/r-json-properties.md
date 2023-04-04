---
title: JSONP屬性
description: 如果將jsonp指定為回應格式，則回覆資料會使用JSONP（含邊框間距的JavaScript物件標籤法）格式化，並包裝在JavaScript函式呼叫中。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2294eb37-b362-438f-94bc-eb24ca641752
source-git-commit: d1df6e943747f9db12c08003647aee840fdfcc0a
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 1%

---

# JSONP屬性{#jsonp-properties}

如果將jsonp指定為回應格式，則回覆資料會使用JSONP（含邊框間距的JavaScript物件標籤法）格式化，並包裝在JavaScript函式呼叫中。

客戶端可以指定可選的唯一請求標識符( *`reqId`*)，這會在回應中傳回，並讓用戶端區分非同步收到的多個回應。 典型回應的一般結構如下：

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

此 `s7jsonResponse` JavaScript函式必須由用戶端定義。 在最簡單的形式中，函式可能如下所示：

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

支援JSONP回應格式的要求可讓您使用的擴充語法，指定JS回呼處理常式的名稱 `req=` 參數：

`req=...,json [&handler = reqHandler]`

此 `<reqHandler>` 語法是JSONP回應中出現的JS處理常式的名稱。 僅允許a-z、A-Z和0-9個字元。 選擇性. 預設為 `s7jsonResponse`.

Dynamic Media影像伺服檢視器套件包含公用程式，可從影像伺服中要求和剖析JSONP格式化資料。

請參閱 [https://en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP) 以取得JSONP格式的詳細資訊。

請參閱 [www.json.org](https://www.json.org/json-en.html) 以取得JSON格式的詳細資訊。

另請參閱 [請求](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76).
