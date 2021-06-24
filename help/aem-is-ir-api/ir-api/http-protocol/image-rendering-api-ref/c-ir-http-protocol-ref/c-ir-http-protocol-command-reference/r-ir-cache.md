---
description: 快取控制。 可選擇性地停用用戶端快取（瀏覽器、代理伺服器、網路快取系統）和內部Platform伺服器快取中的快取。
solution: Experience Manager
title: 快取
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 4745197a-9f2d-4e33-8c0e-0067fbd65254
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 1%

---

# 快取{#cache}

快取控制。 可選擇性地停用用戶端快取（瀏覽器、代理伺服器、網路快取系統）和內部Platform伺服器快取中的快取。

`cache= *`cacheControl`*`

`cache= *``*, *`clientControlserverControl`*`

<table id="simpletable_CBB5DFBD48B444A4AA806B11299BC43E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cacheControl</span> </p> </td> 
  <td class="stentry"> <p>on |關閉 |驗證 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> clientControl  </span> </p> </td> 
  <td class="stentry"> <p>on |關閉 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> serverControl  </span> </p></td> 
  <td class="stentry"> <p>on |關閉 </p></td> 
 </tr> 
</table>

如果只指定了一個&#x200B;*`cacheControl`*&#x200B;值，則該值將同時應用於客戶端和伺服器快取。

「 `validate`」關鍵字允許在紋理或暈映檔案更改後更新伺服器快取條目，而無需等待快取條目自動過期。 此命令不影響客戶端快取。

如果在巢狀請求中指定，`cache=on`會啟用由巢狀請求產生的影像的持續、伺服器端快取。 只有在預期會以完全相同的參數重複呼叫相同的巢狀請求時，才應謹慎啟用巢狀請求的快取。

## 屬性 {#section-0dcbd62e1122400e8c347f408f2d937e}

可能發生在請求中的任何位置。 當要求未傳回回影像時忽略。 *`clientControl`* 當材料目錄停用用戶端快取時(如果 `attribute::Expiration` 有負值)，則會忽略。*`serverControl`* 如果停用伺服器快取，則會忽略( `PlatformServer::cache.enable`)。

## 預設 {#section-9034a1f4d7984c8f8dce3fc1e1803723}

`cache=on,on` 針對HTTP要求， `cache=off` 針對巢狀/內嵌要求。

## 另請參閱 {#section-2f5853751dab49579e97418fa766bdf9}

[目錄：：過期](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce)，請 [求=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
