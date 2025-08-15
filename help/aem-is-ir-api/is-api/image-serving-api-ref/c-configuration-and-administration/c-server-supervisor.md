---
description: 「影像伺服」元件由「伺服器監督員」管理，它是Linux精靈或Windows服務（S7Supervisor.exe，列為「服務控制面板」中的「動態媒體影像伺服」）。
solution: Experience Manager
title: 伺服器監督員
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 83b6a63f-6bb8-4a14-b8d5-389d23fae57c
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---

# 伺服器監督員{#server-supervisor}

「影像伺服」元件由「伺服器監督員」管理，它是Linux精靈或Windows服務（S7Supervisor.exe，列為「服務控制面板」中的「動態媒體影像伺服」）。

除了啟動和停止其他「影像伺服」元件之外，伺服器管理員還負責確保這些其他元件的健康狀態。 若元件當機，就會自動重新啟動，以將任何服務中斷的情況降至最低。

## 啟動和停止 {#section-061d28d74e034a30adc39ea3e2031cd0}

伺服器管理員會使用「影像伺服」公用程式指令碼啟動、停止和重新啟動。 如需詳細資訊，請參閱[公用程式檔案](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)。

啟動和停止「伺服器監督程式」會自動啟動和停止所有其他「影像伺服」元件。

[SupervisorRegistry.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6)
