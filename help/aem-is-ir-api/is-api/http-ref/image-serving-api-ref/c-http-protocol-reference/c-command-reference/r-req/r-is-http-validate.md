---
description: 請求驗證。
seo-description: 請求驗證。
seo-title: 驗證
solution: Experience Manager
title: 驗證
uuid: 5322c484-2cf5-4022-9863-73fc525beb56
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 5%

---


# 驗證{#validate}

請求驗證。

`req=validate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_F214CDA7580A46C0B5CF14CF13AA9B0A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span> </span> </p> </td> 
  <td class="stentry"> <p>唯一的請求識別碼。 </p></td> 
 </tr> 
</table>

分析請求字串的方式就像指定了`req=img`，但不會取代變數並評估參考物件（影像、ICC描述檔、字型等）。 如果解析失敗，則會傳回標準錯誤回應，否則會傳回下列屬性：

`request.isValid=1`

HTTP回應無法快取。

支援JSONP回應格式的請求可讓您使用`req=`參數的擴充語法來指定JS回呼處理常式的名稱：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JS回應中顯示的JS處理常式名稱。僅允許a-z、A-Z和0-9字元。 選填。預設為 `s7jsonResponse`.
