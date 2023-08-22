---
title: 快取
description: 快取控制。 允許選擇性地停用使用者端快取（瀏覽器、Proxy伺服器、網路快取系統）和內部快取 [!DNL Platform Server] 快取。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b631836-e5a8-4a56-a09a-35bb2474cc84
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 1%

---

# 快取{#cache}

快取控制。 允許選擇性地停用使用者端快取（瀏覽器、Proxy伺服器、網路快取系統）和內部快取 [!DNL Platform Server] 快取。

`cache= *`cacheControl`*`

`cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_70ACECAEA02F400C83B598FA13F1D00B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> 開啟|關閉|驗證|更新</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> clientControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 開啟|關閉</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> serverControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 開啟|關閉</span> </p></td> 
 </tr> 
</table>

若只有一個 `*`cacheControl`*` 值已指定，則會同時套用至使用者端和伺服器快取。

此 `validate` 關鍵字允許在影像檔案變更後更新快取專案，不必等待快取專案自動過期。 這個命令不會影響使用者端快取。

此 `update` 關鍵字可用來強制更新伺服器端快取專案。 當資源變更後，如字型檔案修改時未變更其檔案名稱或關聯的字型ID，這很有用，因為快取驗證機制不會直接追蹤這些資源。

若在巢狀要求中指定， `cache=on` 啟用巢狀要求所產生影像的伺服器端持續快取。 只有當同一巢狀要求預期會使用完全相同的引數重複呼叫時，才應該注意啟用巢狀要求的快取。

## 屬性 {#section-dfd0b2f92b3743fc8b9d2c35a786eb81}

要求屬性。 不論目前的圖層設定為何，皆適用。 當要求未傳回回覆影像時忽略。 *`clientControl`*會在影像目錄停用使用者端快取時忽略(如果 `catalog::Expiration` 具有負值)。

使用者端快取控制( `on` 和 `off` 僅限)，也可用於靜態內容請求： [!DNL /is/content/].

## 預設 {#section-4124b2c836e2491489b9009a92fe4f22}

`cache=on,on` 對於HTTP請求， `cache=off` 對於巢狀/內嵌請求， `cache=on` 用於靜態內容請求。

## 另請參閱 {#section-7c2ac171fa0e4aa4a2e9955fd2d2013e}

[catalog：：Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ， [需要=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
