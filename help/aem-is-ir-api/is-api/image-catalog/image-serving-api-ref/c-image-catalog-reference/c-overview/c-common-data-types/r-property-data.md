---
description: 屬性資料包含代表一或多個屬性的文字字串。
solution: Experience Manager
title: 屬性資料
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86278720-ece0-4e67-8fb1-443355f878b7
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---

# 屬性資料{#property-data}

屬性資料包含代表一或多個屬性的文字字串。

屬性由屬性名稱和屬性值組成，以=分隔。

多個屬性由行分隔符號分隔，可能是`??`或`<CR><LF>`。 如果整個屬性資料字串未括在引號中，伺服器會先以`<CR><LF>`取代`??`的每個例項，然後再將資料傳輸至使用者端。 屬性名稱可由字母、數字、&#39;.&#39;、&#39;-&#39;和&#39;_&#39;組成。 屬性名稱不區分大小寫。

屬性值不得包含行分隔符號。

如需套用至屬性資料的其他規則，請參閱[文字字串](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63)。
