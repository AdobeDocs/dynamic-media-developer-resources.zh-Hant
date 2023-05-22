---
description: 請求字串的整個修飾符部分（包括可選的鎖尾碼）的內容可以通過應用標準base64編碼來模糊。
solution: Experience Manager
title: 請求模糊處理
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 358d714b-703d-418b-90c0-5940f5388c7d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 1%

---

# 請求模糊處理{#request-obfuscation}

請求字串的整個修飾符部分（包括可選的鎖尾碼）的內容可以通過應用標準base64編碼來模糊。

如果 `attribute::RequestObfuscation` 的子菜單。 如果解碼失敗，請求將被拒絕。 如果同時應用了請求鎖定和請求混淆，則必須生成鎖定尾碼並在base64編碼之前附加。

>[!IMPORTANT]
>
>如果啟用此功能，請注意其使用存在以下某些限制：<br>-Dynamic Media用戶介面可能未顯示 **[!UICONTROL 上次發佈時間]** 的子菜單。 但是，這種影響不會影響發佈。<br> — 當前，HLS視頻流在 **[!UICONTROL 請求模糊處理]** 和 **[!UICONTROL 請求鎖定]** 的子菜單。<br> — 目前，部分Dynamic Media觀眾在 **[!UICONTROL 請求模糊處理]** 和 **[!UICONTROL 請求鎖定]** 的子菜單。

## 範例 {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

編碼為：

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

在對請求進行模糊處理之前，必須使用「%xx」編碼對值字串中出現的「=」、「&amp;」和「%」進行轉義。 無需進行其它http編碼 *修飾* 在混淆之前或之後請求的一部分，即使應用了請求鎖定，因為base64編碼對http傳輸是安全的。

## 另請參閱 {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[HTTP編碼](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7)。 [請求鎖定](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c)。 [屬性：:RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
