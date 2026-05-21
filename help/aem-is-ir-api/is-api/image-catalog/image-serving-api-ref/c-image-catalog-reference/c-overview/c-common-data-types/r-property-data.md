---
description: 屬性資料包含代表一或多個屬性的文字字串。
solution: Experience Manager
title: 屬性資料
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86278720-ece0-4e67-8fb1-443355f878b7
TQID: 'https://experienceleague.adobe.com/jE8U1fgDsG9wdzG4O-BsPHvPOGLXDxZRMdZvL9LuYZE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 110
ht-degree: 0%

---

# 屬性資料{#property-data}

屬性資料包含代表一或多個屬性的文字字串。

屬性由屬性名稱和屬性值組成，以=分隔。

多個屬性由行分隔符號分隔，可能是`??`或`<CR><LF>`。 如果整個屬性資料字串未括在引號中，伺服器會先以`<CR><LF>`取代`??`的每個例項，然後再將資料傳輸至使用者端。 屬性名稱可由字母、數字、&#39;.&#39;、&#39;-&#39;和&#39;_&#39;組成。 屬性名稱不區分大小寫。

屬性值不得包含行分隔符號。

如需套用至屬性資料的其他規則，請參閱[文字字串](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63)。
