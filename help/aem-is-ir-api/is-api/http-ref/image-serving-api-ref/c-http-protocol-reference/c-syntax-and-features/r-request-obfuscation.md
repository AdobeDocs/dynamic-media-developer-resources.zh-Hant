---
description: 請求字串的整個修飾元部分的內容（包括選用的鎖定字尾）可能會因套用標準base64編碼而被遮住。
solution: Experience Manager
title: 請求模糊化
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 1%

---


# 要求模糊化{#request-obfuscation}

請求字串的整個修飾元部分的內容（包括選用的鎖定字尾）可能會因套用標準base64編碼而被遮住。

如果設定了`attribute::RequestObfuscation`，則伺服器會嘗試解碼。 如果解碼失敗，則會拒絕請求。 如果同時套用請求鎖定和請求模糊化，則必須在base64編碼之前產生並附加鎖定字尾。

>[!IMPORTANT]
>
>如果您啟用此功能，請注意其使用有某些限制，其中包括：<br>-Dynamic Media用戶介面可能無法顯示&#x200B;**[!UICONTROL 上次發佈]**&#x200B;欄位的正確詳細資訊。 不過，這種影響並不會影響發佈。<br>-目前，啟用「請求模糊化」和「請求鎖定」時，**[!UICONTROL HLS]** 視訊 **[!UICONTROL 串流無]** 法運作。<br>-目前，在啟用「請求模糊化」和「請求 **[!UICONTROL 鎖定」]** 時，某些 **[!UICONTROL Dynamic Media]** 檢視器無法運作。

## 範例 {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

編碼為：

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

值字串中出現的&#39;=&#39;、&#39;&amp;&#39;和&#39;%&#39;，必須先使用&#39;%xx&#39;編碼逸出，才能模糊化請求。 即使套用請求鎖定，也不必在模糊化之前或之後，將請求的&#x200B;*修飾詞*&#x200B;部分進行http編碼，因為base64編碼對於http傳輸是安全的。

## 另請參閱 {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[HTTP編碼](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7)，請 [求鎖定](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c)，屬 [性：:RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
