---
description: 快取控制。 可選擇性地停用用戶端快取（瀏覽器、代理伺服器、網路快取系統）和內部Platform伺服器快取中的快取。
solution: Experience Manager
title: 快取
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b631836-e5a8-4a56-a09a-35bb2474cc84
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 1%

---

# 快取{#cache}

快取控制。 可選擇性地停用用戶端快取（瀏覽器、代理伺服器、網路快取系統）和內部Platform伺服器快取中的快取。

`cache= *`cacheControl`*`

`cache= *``*, *`clientControlserverControl`*`

<table id="simpletable_70ACECAEA02F400C83B598FA13F1D00B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> 開啟|關閉|驗證|更新</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> clientControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 開啟/關閉</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> serverControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 開啟/關閉</span> </p></td> 
 </tr> 
</table>

如果只指定了一個`*`cacheControl`*`值，則該值將同時應用於客戶端和伺服器快取。

`validate`關鍵字允許在影像檔案更改後更新快取條目，而無需等待快取條目自動過期。 此命令不影響客戶端快取。

`update`關鍵字可用於強制更新伺服器端快取項。 在資源被更改後（不由快取驗證機制直接跟蹤），例如在修改字型檔案而不更改其檔案名或相關字型ID時，這很有用。

如果在巢狀請求中指定，`cache=on`會啟用由巢狀請求產生的影像的持續、伺服器端快取。 只有在預期會以完全相同的參數重複呼叫相同的巢狀請求時，才應謹慎啟用巢狀請求的快取。

## 屬性 {#section-dfd0b2f92b3743fc8b9d2c35a786eb81}

要求屬性。 無論目前的層設定為何皆適用。 當要求未傳回回影像時忽略。 當影像目錄停用用戶端快取時（如果`catalog::Expiration`有負值），會忽略*`clientControl`*。

用戶端快取控制項（僅`on`和`off`）也可用於[!DNL /is/content/]的靜態內容請求。

## 預設 {#section-4124b2c836e2491489b9009a92fe4f22}

`cache=on,on` 針對HTTP要求、 `cache=off` 巢狀/內嵌要求、 `cache=on` 靜態內容要求。

## 另請參閱 {#section-7c2ac171fa0e4aa4a2e9955fd2d2013e}

[目錄：：過期](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ，請 [求=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
