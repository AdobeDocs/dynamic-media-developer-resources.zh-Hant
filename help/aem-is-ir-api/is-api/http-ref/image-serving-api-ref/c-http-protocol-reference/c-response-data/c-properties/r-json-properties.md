---
description: 如果將jsonp指定為回應格式，則回覆資料會使用JSONP（含填充的JavaScript物件記號）格式化，並封裝在JavaScript函式呼叫中。
solution: Experience Manager
title: JSONP屬性
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 1%

---


# JSONP屬性{#jsonp-properties}

如果將jsonp指定為回應格式，則回覆資料會使用JSONP（含填充的JavaScript物件記號）格式化，並封裝在JavaScript函式呼叫中。

客戶機可以指定可選的唯一請求標識符(*`reqId`*)，該標識符在響應中返回並允許客戶機區分非同步接收的多個響應。 典型響應具有以下一般結構：

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

支援JSONP回應格式的請求可讓您使用`req=`參數的擴充語法來指定JS回呼處理常式的名稱：

`req=...,json [&handler = reqHandler]`

`<reqHandler>` 是JS回應中顯示的JS處理常式名稱。僅允許a-z、A-Z和0-9字元。 選填。預設為 `s7jsonResponse`.

Dynamic Media映像服務查看器軟體包包含一個實用程式，用於從映像服務請求和解析JSONP格式的資料。

有關JSONP格式的詳細資訊，請參見[http://en.wikipedia.org/wiki/JSONP](http://en.wikipedia.org/wiki/JSONP)。

如需JSON格式的詳細資訊，請參閱[www.json.org](http://www.json.org)。

另請參閱[req](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)。
