---
description: 快取控制。 允許有選擇地禁用內部中的客戶端快取（瀏覽器、代理伺服器、網路快取系統）和快取 [!DNL Platform Server] 快取。
solution: Experience Manager
title: 快取
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b631836-e5a8-4a56-a09a-35bb2474cc84
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 1%

---

# 快取{#cache}

快取控制。 允許有選擇地禁用內部中的客戶端快取（瀏覽器、代理伺服器、網路快取系統）和快取 [!DNL Platform Server] 快取。

`cache= *`快取控制`*`

`cache= *`客戶端控制項`*, *`伺服器控制`*`

<table id="simpletable_70ACECAEA02F400C83B598FA13F1D00B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 快取控制</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> 關閉|驗證|更新</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 客戶端控制項</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 關</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 伺服器控制</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 關</span> </p></td> 
 </tr> 
</table>

如果只有一個 `*`快取控制`*` 值已指定，它應用於客戶端和伺服器快取。

的 `validate` 關鍵字允許在映像檔案更改後更新快取項，而無需等待快取項自動過期。 客戶端快取不受此命令的影響。

的 `update` 關鍵字可用於強制更新伺服器端快取項。 在更改了不直接由快取驗證機制跟蹤的資源後，這非常有用，例如修改字型檔案時，不更改其檔案名或關聯的字型ID。

如果在嵌套請求中指定， `cache=on` 啟用嵌套請求生成的影像的持久性伺服器端快取。 只有當期望使用完全相同的參數重複調用同一嵌套請求時，才應注意啟用嵌套請求的快取。

## 屬性 {#section-dfd0b2f92b3743fc8b9d2c35a786eb81}

請求屬性。 應用，與當前圖層設定無關。 當請求未返回回復影像時忽略。 *`clientControl`當映像目錄禁用客戶端快取時(如果 `catalog::Expiration` 為負值)。

客戶端快取控制( `on` 和 `off` 僅)也可用於以下位置的靜態內容請求 [!DNL /is/content/]。

## 預設 {#section-4124b2c836e2491489b9009a92fe4f22}

`cache=on,on` 對於HTTP請求， `cache=off` 嵌套/嵌入式請求， `cache=on` 為靜態內容請求。

## 另請參閱 {#section-7c2ac171fa0e4aa4a2e9955fd2d2013e}

[目錄：：到期](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) 。 [請求=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
