---
description: 屬性資料包含代表一或多個屬性的文字字串。
solution: Experience Manager
title: 屬性資料
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 86278720-ece0-4e67-8fb1-443355f878b7
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---

# 屬性資料{#property-data}

屬性資料包含代表一或多個屬性的文字字串。

屬性包含屬性名稱和屬性值，由=分隔。

多個屬性以行分隔符分隔，行分隔符可以是`??`或`<CR><LF>`。 如果整個屬性資料字串未括在引號中，則伺服器會先將`??`的每個出現次數以`<CR><LF>`取代，再將資料傳送至用戶端。 屬性名稱可能包含字母、數字、「。」、「 — 」和「_」。 屬性名稱不區分大小寫。

屬性值不得包含行分隔符號。

如需套用至屬性資料的其他規則，請參閱[文字字串](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63)。
