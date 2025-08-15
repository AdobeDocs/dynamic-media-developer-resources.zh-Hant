---
title: 快取
description: 快取控制。 允許選擇性地停用使用者端快取（瀏覽器、Proxy伺服器、網路快取系統）和內部 [!DNL Platform Server] 快取中的快取。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4745197a-9f2d-4e33-8c0e-0067fbd65254
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 1%

---

# 快取 {#cache}

快取控制。 可讓您選擇性地停用使用者端快取（瀏覽器、Proxy伺服器、網路快取系統）以及內部[!DNL Platform Server]快取中的快取。

`cache= *`cacheControl`*`

`cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_CBB5DFBD48B444A4AA806B11299BC43E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cacheControl</span> </p> </td> 
  <td class="stentry"> <p>於 | 關閉 | 驗證 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> clientControl </span> </p> </td> 
  <td class="stentry"> <p>於 | 關閉 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> serverControl </span> </p></td> 
  <td class="stentry"> <p>於 | 關閉 </p></td> 
 </tr> 
</table>

如果只指定一個&#x200B;*`cacheControl`*&#x200B;值，則會同時套用至使用者端和伺服器快取。

&#39;`validate`&#39;關鍵字允許在紋理或暈映檔案變更後更新伺服器快取專案，而不需等待快取專案自動過期。 這個命令不會影響使用者端快取。

如果在巢狀要求中指定，`cache=on`會啟用巢狀要求所產生影像的伺服器端持續快取。 請注意，只有當使用相同引數重複呼叫相同的巢狀要求時，才能啟用巢狀要求的快取。

## 屬性 {#section-0dcbd62e1122400e8c347f408f2d937e}

可能發生在請求中的任何位置。 當要求未傳回回覆影像時忽略。 當資料目錄停用使用者端快取時（如果&#x200B;*`clientControl`*&#x200B;具有負值），會忽略屬性`attribute::Expiration`。 如果停用伺服器快取( *`serverControl`*)，則會忽略屬性`PlatformServer::cache.enable`。

## 預設 {#section-9034a1f4d7984c8f8dce3fc1e1803723}

`cache=on,on`若是HTTP要求，`cache=off`若是巢狀/內嵌要求。

## 另請參閱 {#section-2f5853751dab49579e97418fa766bdf9}

[目錄：：Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce)，[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
