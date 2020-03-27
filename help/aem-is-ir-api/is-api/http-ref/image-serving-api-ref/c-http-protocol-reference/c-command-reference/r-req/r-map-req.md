---
description: 影像地圖資料。
seo-description: 影像地圖資料。
seo-title: 地圖
solution: Experience Manager
title: 地圖
topic: Scene7 Image Serving - Image Rendering API
uuid: 57cb0fcf-5a07-4109-bfd4-ef9aaf794b27
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 地圖{#map}

影像地圖資料。

`req=map[,text|{xml[, *`EncodingreqId`*]}|{json[&id= *``*]}]`

<table id="simpletable_10F2152FDF33411491FBBAFD173CA5ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 編碼</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8| UTF-16| UTF-16LE| UTF-16BE| ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>唯一的請求識別碼。 </p></td> 
 </tr> 
</table>

在查 `catalog::Map` 詢沒有指定其他命令的簡單目錄條目時（不會縮放為），返回不進行 `catalog::maxPix`修改。

如果請求中指定了任何其他命令，則會傳回合成影像地圖，其衍生方式是縮放、裁切、旋轉和分層請求中包含的所有 `catalog::Map` 和/ `map=` /或命令，就像影像資料一樣 `req=img`。

指定 `text` 或省略第二個參數，以具有回應MIME類型的元素字串形式傳 `HTML <AREA>` 回影像地圖資料 `text/plain`。

指定 `xml` 以XML格式化回應，而非HTML。 可選擇指定文字編碼。 預設值為 `UTF-8`.

如果找不到指定目錄物件的對 `<AREA>` 應資料，且／或在裁切影像後未保留任何元素，則傳回空字串( `<AREA>` 或空元素)。

The HTTP response is cacheable with the TTL based on `catalog::Expiration`.

支援JSONP回應格式的請求可讓您使用參數的擴充語法來指定JS回呼處理常式 `req=` 的名稱：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JS回應中顯示的JS處理常式名稱。 僅允許a-z、A-Z和0-9字元。 選填。預設為 `s7jsonResponse`.

See [Image Maps](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab).
