---
description: 為了減少篡改請求的機會，提供了簡單的鎖定裝置。
solution: Experience Manager
title: 請求鎖定
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7ac727ef-3775-4884-b9db-bfae171a0f9d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# 請求鎖定{#request-locking}

為了減少篡改請求的機會，提供了簡單的鎖定裝置。

如果設定了屬性：:RequestLock，則必須將鎖定值附加到請求，其形式為`&xxxx`，其中xxxx為四位數的十六進位值。 此十六進位值是使用套用至請求的&#x200B;*modifiers*&#x200B;部分（在「？」後）的簡單雜湊演算法產生 將URL路徑與&#x200B;*修飾元*&#x200B;分開。 這必須在要求完全http編碼後完成，但必須在要求模糊化前完成（選擇性）。 將請求去模糊化後，伺服器會對修飾詞字串使用相同的雜湊演算法（不包括最後5個字元，其中包含鎖定值）。 如果產生的金鑰不符合鎖定，則拒絕要求。

>[!IMPORTANT]
>
>若您啟用此功能，請注意其使用方式有某些限制，包括：<br>- Dynamic Media使用者介面可能未顯示&#x200B;**[!UICONTROL 上次發佈]**&#x200B;欄位的正確詳細資料。 不過，此影響不會影響發佈。<br> — 目前，啟用請求模糊化和請&#x200B;**[!UICONTROL 求鎖]** 定時， **[!UICONTROL HLS視]** 訊串流無法運作。<br> — 目前，啟用「要求模糊化」和「要 **[!UICONTROL 求鎖]** 定」時， **[!UICONTROL 有些Dynamic Media]** 檢視器無法運作。

C++產生請求鎖定值的范常式式碼：

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

[HTTP編碼](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7)，請 [求模糊化](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d), [屬性：:RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
