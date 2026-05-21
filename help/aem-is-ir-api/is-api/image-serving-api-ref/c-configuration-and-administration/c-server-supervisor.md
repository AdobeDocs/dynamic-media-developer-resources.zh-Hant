---
description: 「影像伺服」元件由「伺服器監督員」管理，它是Linux精靈或Windows服務（S7Supervisor.exe，列為「服務控制面板」中的「動態媒體影像伺服」）。
solution: Experience Manager
title: 伺服器監督員
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 83b6a63f-6bb8-4a14-b8d5-389d23fae57c
TQID: 'https://experienceleague.adobe.com/D3cGGQLVly7MwWSvSjkWcWkuR9kVUFC9sSvItZm6eOc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 138
ht-degree: 0%

---

# 伺服器監督員{#server-supervisor}

「影像伺服」元件由「伺服器監督員」管理，它是Linux精靈或Windows服務（S7Supervisor.exe，列為「服務控制面板」中的「動態媒體影像伺服」）。

除了啟動和停止其他「影像伺服」元件之外，伺服器管理員還負責確保這些其他元件的健康狀態。 若元件當機，就會自動重新啟動，以將任何服務中斷的情況降至最低。

## 啟動和停止 {#section-061d28d74e034a30adc39ea3e2031cd0}

伺服器管理員會使用「影像伺服」公用程式指令碼啟動、停止和重新啟動。 如需詳細資訊，請參閱[公用程式檔案](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)。

啟動和停止「伺服器監督程式」會自動啟動和停止所有其他「影像伺服」元件。

[SupervisorRegistry.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6)
