---
description: 為了減少篡改請求的機會，提供了一種簡單的鎖定裝置。
solution: Experience Manager
title: 請求鎖定
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7ac727ef-3775-4884-b9db-bfae171a0f9d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# 請求鎖定{#request-locking}

為了減少篡改請求的機會，提供了一種簡單的鎖定裝置。

如果設定了屬性：:RequestLock，則必須將鎖定值以以下形式附加到請求 `&xxxx`，其中xxx是四位十六進位值。 此十六進位值是使用應用於 *修飾* 請求的一部分（在「？」之後） 將URL路徑與 *修飾*)。 必須在請求完全HTTP編碼後，但在請求被（可選）模糊之前完成此操作。 在對請求進行去模糊處理後，伺服器將對修飾符字串使用相同的散列算法（不包括包含鎖定值的最後5個字元）。 如果生成的密鑰與鎖不匹配，則請求被拒絕。

>[!IMPORTANT]
>
>如果啟用此功能，請注意其使用存在以下某些限制：<br>-Dynamic Media用戶介面可能未顯示 **[!UICONTROL 上次發佈時間]** 的子菜單。 但是，這種影響不會影響發佈。<br> — 當前，HLS視頻流在 **[!UICONTROL 請求模糊處理]** 和 **[!UICONTROL 請求鎖定]** 的子菜單。<br> — 目前，部分Dynamic Media觀眾在 **[!UICONTROL 請求模糊處理]** 和 **[!UICONTROL 請求鎖定]** 的子菜單。

生成請求鎖定值的C++示例代碼：

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

[HTTP編碼](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7)。 [請求模糊處理](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d)。 [屬性：:RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
