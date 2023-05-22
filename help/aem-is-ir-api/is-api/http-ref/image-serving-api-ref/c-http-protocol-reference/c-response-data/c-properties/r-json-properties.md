---
title: JSONP屬性
description: 如果將jsonp指定為響應格式，則使用JSONP（帶填充的JavaScript對象表示法）對答復資料進行格式化，並包裝在JavaScript函式調用中。
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

如果將jsonp指定為響應格式，則使用JSONP（帶填充的JavaScript對象表示法）對答復資料進行格式化，並包裝在JavaScript函式調用中。

客戶機可指定可選的唯一請求標識符( *`reqId`*)，它在響應中返回，允許客戶端區分非同步接收的多個響應。 典型響應具有以下一般結構：

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

的 `s7jsonResponse` JavaScript函式必須由客戶端定義。 在最簡單的形式中，函式可能如下所示：

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

支援JSONP響應格式的請求允許您使用擴展語法指定JS回調處理程式的名稱 `req=` 參數：

`req=...,json [&handler = reqHandler]`

的 `<reqHandler>` 語法是JSONP響應中存在的JS處理程式的名稱。 只允許使用a-z、A-Z和0-9個字元。 選擇性. 預設為 `s7jsonResponse`.

Dynamic Media影像服務查看器包包括用於從影像服務請求和分析JSONP格式的資料的實用程式。

請參閱 [https://en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP) 的子菜單。

請參閱 [www.json.org](https://www.json.org/json-en.html) 的子菜單。

另請參閱 [請求](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)。
