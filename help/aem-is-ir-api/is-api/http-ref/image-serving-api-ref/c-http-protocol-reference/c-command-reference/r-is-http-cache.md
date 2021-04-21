---
description: 快取控制。 允許選擇性地停用內部平台伺服器快取中的用戶端快取（瀏覽器、代理伺服器、網路快取系統）和快取。
solution: Experience Manager
title: 快取
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 1%

---


# cache{#cache}

快取控制。 允許選擇性地停用內部平台伺服器快取中的用戶端快取（瀏覽器、代理伺服器、網路快取系統）和快取。

`cache= *`cacheControl`*`

`cache= *`clientControlserverControl`*, *``*`

<table id="simpletable_70ACECAEA02F400C83B598FA13F1D00B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> on|off|validate|update</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> clientControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 開啟／關閉</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> serverControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 開啟／關閉</span> </p></td> 
 </tr> 
</table>

如果只指定一個`*`cacheControl`*`值，則該值將同時應用於客戶機和伺服器快取。

`validate`關鍵字允許在映像檔案更改後更新快取條目，而無需等待快取條目自動過期。 用戶端快取不受此命令的影響。

`update`關鍵字可用來強制更新伺服器端快取項目。 當資源變更後，這些資源不會直接由快取驗證機制追蹤，例如在修改字型檔案時，不變更其檔案名稱或相關的字型ID。

如果在巢狀請求中指定，`cache=on`會啟用由巢狀請求產生的影像的持續伺服器端快取。 請務必注意，只有當相同的巢狀請求預期會以完全相同的參數重複呼叫時，才會啟用巢狀請求的快取。

## 屬性 {#section-dfd0b2f92b3743fc8b9d2c35a786eb81}

請求屬性。 不論目前的圖層設定如何，都適用。 當請求未傳回回回覆影像時忽略。 *`clientControl`*會在影像目錄停用用戶端快取時忽略（如果`catalog::Expiration`有負值）。

用戶端快取控制（僅限`on`和`off`）也適用於[!DNL /is/content/]的靜態內容要求。

## 預設 {#section-4124b2c836e2491489b9009a92fe4f22}

`cache=on,on` 對於HTTP請求、 `cache=off` 巢狀／內嵌請求、靜 `cache=on` 態內容請求。

## 另請參閱 {#section-7c2ac171fa0e4aa4a2e9955fd2d2013e}

[目錄：:Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ,  [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
