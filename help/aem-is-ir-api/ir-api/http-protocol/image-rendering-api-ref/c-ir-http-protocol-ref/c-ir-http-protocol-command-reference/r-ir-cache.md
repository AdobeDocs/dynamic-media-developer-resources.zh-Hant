---
title: 快取
description: 快取控制。 可選擇性地停用內部的用戶端快取（瀏覽器、代理伺服器、網路快取系統）和快取 [!DNL Platform Server] 快取。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4745197a-9f2d-4e33-8c0e-0067fbd65254
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 2%

---

# 快取 {#cache}

快取控制。 可讓您選擇性停用內部的用戶端快取（瀏覽器、代理伺服器、網路快取系統）和快取 [!DNL Platform Server] 快取。

`cache= *`cacheControl`*`

`cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_CBB5DFBD48B444A4AA806B11299BC43E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cacheControl</span> </p> </td> 
  <td class="stentry"> <p>on |關閉 |驗證 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> clientControl </span> </p> </td> 
  <td class="stentry"> <p>on |關閉 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> serverControl </span> </p></td> 
  <td class="stentry"> <p>on |關閉 </p></td> 
 </tr> 
</table>

如果只有一個 *`cacheControl`* 值時，該值將同時應用於客戶端和伺服器快取。

「 `validate`「關鍵字」允許在紋理或暈映檔案更改後更新伺服器快取條目，而無需等待快取條目自動過期。 此命令不影響客戶端快取。

若在巢狀請求中指定， `cache=on` 可讓巢狀請求產生的影像在伺服器端持續快取。 請注意，只有當使用相同參數重複呼叫相同巢狀請求時，才會啟用巢狀請求的快取。

## 屬性 {#section-0dcbd62e1122400e8c347f408f2d937e}

可能發生在請求中的任何位置。 當要求未傳回回影像時忽略。 屬性 *`clientControl`* 當材料目錄停用用戶端快取時(如果 `attribute::Expiration` 為負值)。 屬性 *`serverControl`* 如果停用伺服器快取，則會忽略( `PlatformServer::cache.enable`)。

## 預設 {#section-9034a1f4d7984c8f8dce3fc1e1803723}

`cache=on,on` 若為HTTP要求， `cache=off` 的URL。

## 另請參閱 {#section-2f5853751dab49579e97418fa766bdf9}

[目錄：：過期](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
