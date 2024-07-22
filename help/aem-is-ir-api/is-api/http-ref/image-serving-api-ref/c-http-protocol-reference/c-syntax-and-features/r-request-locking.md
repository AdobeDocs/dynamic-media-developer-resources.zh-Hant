---
description: 為了減少篡改請求的機會，提供簡單的鎖定工具。
solution: Experience Manager
title: 要求鎖定
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7ac727ef-3775-4884-b9db-bfae171a0f9d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# 要求鎖定{#request-locking}

為了減少篡改請求的機會，提供簡單的鎖定工具。

如果設定了attribute：：RequestLock，則必須以`&xxxx`的格式將鎖定值附加至請求，其中xxxx為四位數的十六進位值。 這個十六進位值是使用套用至要求&#x200B;*修飾元*&#x200B;部分的簡單雜湊演演算法所產生（在&#39;？&#39;之後） 會將URL路徑與&#x200B;*修飾元*&#x200B;分開。 這必須在要求完全經過http編碼之後，但在其（可選）模糊化之前完成。 將請求去模糊化後，伺服器會針對修飾元字串使用相同的雜湊演演算法（排除最後5個字元，其中包含鎖定值）。 如果產生的鍵與鎖定不符，則會拒絕要求。

>[!IMPORTANT]
>
>如果您啟用此功能，請注意，其使用方式有一些限制，包括下列專案：<br>- Dynamic Media使用者介面可能無法顯示&#x200B;**[!UICONTROL 上次發佈]**&#x200B;欄位的正確詳細資料。 不過，這不會影響發佈。<br> — 目前，啟用&#x200B;**[!UICONTROL 要求模糊化]**&#x200B;和&#x200B;**[!UICONTROL 要求鎖定]**&#x200B;時，HLS視訊串流無法運作。<br> — 目前，有些Dynamic Media檢視器在啟用&#x200B;**[!UICONTROL 要求模糊化]**&#x200B;和&#x200B;**[!UICONTROL 要求鎖定]**&#x200B;時無法運作。

產生請求鎖定值的C++範常式式碼：

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

[HTTP編碼](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7)，[要求模糊化](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d)，[屬性：：RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
