---
description: 為了減少篡改請求的機會，提供了簡單的鎖定設備。
seo-description: 為了減少篡改請求的機會，提供了簡單的鎖定設備。
seo-title: 請求鎖定
solution: Experience Manager
title: 請求鎖定
topic: Scene7 Image Serving - Image Rendering API
uuid: 03239376-1e40-48d2-a396-c276802854ed
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 請求鎖定{#request-locking}

為了減少篡改請求的機會，提供了簡單的鎖定設備。

如果設定屬性：:RequestLock，則必須以xxxx為四位十六進位值的形式將鎖定值附加 `&xxxx`至請求。 此十六進位值是使用套用至請求修飾元 *部分* （在&#39;?&#39;之後）的簡單雜湊演算法產生 將URL路徑與修飾元分 *隔*)。 這必須在請求完全http編碼後，但在其被模糊化之前（可選）完成。 在取消對請求進行模糊處理後，伺服器會在修飾詞字串上使用相同的雜湊演算法（排除最後5個字元，其中包含鎖定值）。 如果產生的金鑰不符合鎖定，則會拒絕請求。

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
