---
description: 屬性資料由表示一個或多個屬性的文本字串組成。
solution: Experience Manager
title: 屬性資料
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86278720-ece0-4e67-8fb1-443355f878b7
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---

# 屬性資料{#property-data}

屬性資料由表示一個或多個屬性的文本字串組成。

屬性由屬性名稱和屬性值組成，並以=分隔。

多個屬性由行分隔符分隔，行分隔符可以是 `??` 或 `<CR><LF>`。 如果整個屬性資料字串未用引號括起來，則伺服器將替換 `??` 與 `<CR><LF>` 將資料傳輸到客戶端之前。 屬性名稱可能由字母、數字、「。」、「 — 」和「_」組成。 屬性名稱不區分大小寫。

屬性值不得包括行分隔符。

請參閱 [文本字串](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63) 適用於屬性資料的其他規則。
