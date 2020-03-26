---
description: 如果將jsonp指定為回應格式，則回覆資料會使用JSONP（含填充的JavaScript物件記號）格式化，並封裝在JavaScript函式呼叫中。
seo-description: 如果將jsonp指定為回應格式，則回覆資料會使用JSONP（含填充的JavaScript物件記號）格式化，並封裝在JavaScript函式呼叫中。
seo-title: JSONP屬性
solution: Experience Manager
title: JSONP屬性
topic: Scene7 Image Serving - Image Rendering API
uuid: e53d75f2-9b43-4e8f-8191-66f69f344cdd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# JSONP屬性{#jsonp-properties}

如果將jsonp指定為回應格式，則回覆資料會使用JSONP（含填充的JavaScript物件記號）格式化，並封裝在JavaScript函式呼叫中。

客戶機可指定可選的唯一請求標識符( *`reqId`*)，該標識符在響應中返回並允許客戶機區分非同步接收的多個響應。 典型響應具有以下一般結構：

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

JavaScript `s7jsonResponse` 函式必須由用戶端定義。 在最簡單的形式中，函式可能如下所示：

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

支援JSONP回應格式的請求可讓您使用參數的擴充語法來指定JS回呼處理常式 `req=` 的名稱：

`req=...,json [&handler = reqHandler]`

`<reqHandler>` 是JS回應中顯示的JS處理常式名稱。 僅允許a-z、A-Z和0-9字元。 選填。預設為 `s7jsonResponse`.

Scene7 Image Serving Viewers套件包含一個公用程式，可從Image Serving要求和剖析JSONP格式的資料。

如需 [JSONP格式的詳細資訊](http://en.wikipedia.org/wiki/JSONP) ，請參閱http://en.wikipedia.org/wiki/JSONP。

如需 [JSON格式的詳細資訊](http://www.json.org) ，請參閱www.json.org。

另請參 [閱](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)。
