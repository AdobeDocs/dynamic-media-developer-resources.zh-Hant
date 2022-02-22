---
title: 快取
description: 快取控制。 允許有選擇地禁用客戶端快取（瀏覽器、代理伺服器、網路快取系統）和內部平台伺服器快取中的快取。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4745197a-9f2d-4e33-8c0e-0067fbd65254
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 1%

---

# 快取 {#cache}

快取控制。 用於有選擇地禁用內部平台伺服器快取中的客戶端快取（瀏覽器、代理伺服器、網路快取系統）和快取。

`cache= *`快取控制`*`

`cache= *`客戶端控制項`*, *`伺服器控制`*`

<table id="simpletable_CBB5DFBD48B444A4AA806B11299BC43E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 快取控制</span> </p> </td> 
  <td class="stentry"> <p>上 |關閉 |驗證 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 客戶端控制項 </span> </p> </td> 
  <td class="stentry"> <p>上 |關閉 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 伺服器控制 </span> </p></td> 
  <td class="stentry"> <p>上 |關閉 </p></td> 
 </tr> 
</table>

如果只有一個 *`cacheControl`* 值已指定，它應用於客戶端和伺服器快取。

&#39; `validate`「關鍵字允許在紋理或視頻檔案更改後更新伺服器快取條目，而無需等待快取條目自動過期。 客戶端快取不受此命令的影響。

如果在嵌套請求中指定， `cache=on` 啟用嵌套請求生成的影像的持久性伺服器端快取。 請注意，僅當使用相同的參數重複調用同一嵌套請求時才啟用嵌套請求的快取。

## 屬性 {#section-0dcbd62e1122400e8c347f408f2d937e}

請求中的任何位置都可能發生。 當請求未返回回復影像時忽略。 屬性 *`clientControl`* 當物料目錄禁用客戶端快取時忽略(如果 `attribute::Expiration` 為負值)。 屬性 *`serverControl`* 如果已禁用伺服器快取，則忽略( `PlatformServer::cache.enable`)。

## 預設 {#section-9034a1f4d7984c8f8dce3fc1e1803723}

`cache=on,on` 對於HTTP請求， `cache=off` 嵌套/嵌入式請求。

## 另請參閱 {#section-2f5853751dab49579e97418fa766bdf9}

[目錄：：到期](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce)。 [請求=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
