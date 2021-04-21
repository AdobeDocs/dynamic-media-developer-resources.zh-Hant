---
description: 為了減少篡改請求的機會，提供了簡單的鎖定設備。
solution: Experience Manager
title: 請求鎖定
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---


# 請求鎖定{#request-locking}

為了減少篡改請求的機會，提供了簡單的鎖定設備。

如果設定屬性：:RequestLock，則必須以`&xxxx`的形式將鎖定值附加至請求，其中xxxx為四位十六進位值。 此十六進位值是使用套用至要求之&#x200B;*修飾元*&#x200B;部分（在&#39;?&#39;之後）的簡單雜湊演算法產生 將URL路徑與&#x200B;*修飾詞*&#x200B;分隔。 這必須在請求完全http編碼後，但在其被模糊化之前（可選）完成。 在取消對請求進行模糊處理後，伺服器會在修飾詞字串上使用相同的雜湊演算法（排除最後5個字元，其中包含鎖定值）。 如果產生的金鑰不符合鎖定，則會拒絕請求。

>[!IMPORTANT]
>
>如果您啟用此功能，請注意其使用有某些限制，其中包括：<br>-Dynamic Media用戶介面可能無法顯示&#x200B;**[!UICONTROL 上次發佈]**&#x200B;欄位的正確詳細資訊。 不過，這種影響並不會影響發佈。<br>-目前，啟用「請求模糊化」和「請求鎖定」時，**[!UICONTROL HLS]** 視訊 **[!UICONTROL 串流無]** 法運作。<br>-目前，在啟用「請求模糊化」和「請求 **[!UICONTROL 鎖定」]** 時，某些 **[!UICONTROL Dynamic Media]** 檢視器無法運作。

C++范常式式碼，以產生請求鎖定值：

```
unsigned int lockValue(const char *str) 
{ 
    unsigned int sum = 0; 
    if (str == NULL) 
        return sum; 
    for (; *str; ++str) 
        sum = (sum*131 + *str) & 0xffff; 
    return sum; 
} 
```

## 另請參閱 {#section-a6d45406c0354669ac581793e4fa8436}

[HTTP編碼](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7)，請 [求模糊化](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d)，屬 [性：:RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
