---
description: 快取控制。 允許選擇性地停用內部平台伺服器快取中的用戶端快取（瀏覽器、代理伺服器、網路快取系統）和快取。
solution: Experience Manager
title: 快取
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 1%

---


# cache{#cache}

快取控制。 允許選擇性地停用內部平台伺服器快取中的用戶端快取（瀏覽器、代理伺服器、網路快取系統）和快取。

`cache= *`cacheControl`*`

`cache= *`clientControlserverControl`*, *``*`

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

如果只指定一個&#x200B;*`cacheControl`*&#x200B;值，則它將同時應用於客戶機和伺服器快取。

「 `validate`」關鍵字允許在紋理或暈映檔案更改後更新伺服器快取條目，而無需等待快取條目自動過期。 用戶端快取不受此命令的影響。

如果在巢狀請求中指定，`cache=on`會啟用由巢狀請求產生的影像的持續伺服器端快取。 請務必注意，只有當相同的巢狀請求預期會以完全相同的參數重複呼叫時，才會啟用巢狀請求的快取。

## 屬性 {#section-0dcbd62e1122400e8c347f408f2d937e}

可能發生在請求中的任何位置。 當請求未傳回回回覆影像時忽略。 *`clientControl`* 當材質目錄停用用戶端快取時(如果 `attribute::Expiration` 有負值)會忽略。*`serverControl`* 會在伺服器快取停用( `PlatformServer::cache.enable`)時忽略。

## 預設 {#section-9034a1f4d7984c8f8dce3fc1e1803723}

`cache=on,on` 對於HTTP請求，對 `cache=off` 於巢狀／內嵌請求。

## 另請參閱 {#section-2f5853751dab49579e97418fa766bdf9}

[目錄：:Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce),  [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
