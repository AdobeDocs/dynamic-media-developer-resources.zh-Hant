---
description: 屬性資料由代表一或多個屬性的文字字串組成。
solution: Experience Manager
title: 屬性資料
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---


# 屬性資料{#property-data}

屬性資料由代表一或多個屬性的文字字串組成。

屬性由屬性名稱和屬性值組成，以=分隔。

多個屬性由行分隔符分隔，行分隔符可以是`??`或`<CR><LF>`。 如果整個屬性資料字串未用引號括住，則伺服器會在將資料發送到客戶端之前，用`<CR><LF>`替換每個`??`出現的值。 屬性名稱可能由字母、數字、&#39;.&#39;、&#39;-&#39;和&#39;_&#39;組成。 屬性名稱不區分大小寫。

屬性值不能包含行分隔符。

如需套用至屬性資料的其他規則，請參閱[文字字串](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63)。
