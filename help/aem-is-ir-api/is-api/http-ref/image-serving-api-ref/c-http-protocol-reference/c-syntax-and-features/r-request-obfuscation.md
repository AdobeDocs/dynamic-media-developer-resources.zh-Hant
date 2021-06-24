---
description: 請求字串的整個修飾元部分的內容（包括可選的鎖定尾碼）可能會因套用標準base64編碼而模糊。
solution: Experience Manager
title: 要求模糊化
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 358d714b-703d-418b-90c0-5940f5388c7d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 1%

---

# 要求模糊化{#request-obfuscation}

請求字串的整個修飾元部分的內容（包括可選的鎖定尾碼）可能會因套用標準base64編碼而模糊。

如果設定了`attribute::RequestObfuscation`，則伺服器會嘗試解碼。 如果解碼失敗，則拒絕請求。 如果同時套用要求鎖定和要求模糊化，則必須產生鎖定尾碼並附加在base64編碼之前。

>[!IMPORTANT]
>
>若您啟用此功能，請注意其使用方式有某些限制，包括：<br>- Dynamic Media使用者介面可能未顯示&#x200B;**[!UICONTROL 上次發佈]**&#x200B;欄位的正確詳細資料。 不過，此影響不會影響發佈。<br> — 目前，啟用請求模糊化和請&#x200B;**[!UICONTROL 求鎖]** 定時， **[!UICONTROL HLS視]** 訊串流無法運作。<br> — 目前，啟用「要求模糊化」和「要 **[!UICONTROL 求鎖]** 定」時， **[!UICONTROL 有些Dynamic Media]** 檢視器無法運作。

## 範例 {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

編碼為：

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

值字串中「=」、「&amp;」和「%」的任何出現次數，都必須使用「%xx」編碼進行逸出，才能模糊化請求。 在模糊化之前或之後，也不需要以其他方式將請求的&#x200B;*modifiers*&#x200B;部分進行http編碼，即使已套用請求鎖定，因為base64編碼對於http傳輸是安全的。

## 另請參閱 {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[HTTP Encoding](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7),  [Request Locking](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c),  [attribute::RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
