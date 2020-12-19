---
description: 映像服務元件由Server Supervisor管理，該伺服器Supervisor是Linux守護程式或Windows服務（S7Supervisor.exe，在「服務」控制面板中列為「Scene7 Image Serving」）。
seo-description: 映像服務元件由Server Supervisor管理，該伺服器Supervisor是Linux守護程式或Windows服務（S7Supervisor.exe，在「服務」控制面板中列為「Scene7 Image Serving」）。
seo-title: 伺服器主管
solution: Experience Manager
title: 伺服器主管
topic: Scene7 Image Serving - Image Rendering API
uuid: 6ac38d90-00ed-4d49-84f0-2e77e7a86d47
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# 伺服器主管{#server-supervisor}

映像服務元件由Server Supervisor管理，該伺服器Supervisor是Linux守護程式或Windows服務（S7Supervisor.exe，在「服務」控制面板中列為「Scene7 Image Serving」）。

除了啟動和停止其他映像服務元件外，伺服器主管還負責確保這些元件的運行狀況。 如果元件發生崩潰，則會自動重新啟動它，以最大限度地減少任何服務中斷。

## 啟動和停止{#section-061d28d74e034a30adc39ea3e2031cd0}

使用Image Serving實用程式指令碼啟動、停止和重新啟動伺服器管理器。 如需詳細資訊，請參閱[公用程式檔案](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)。

啟動和停止Server Supervisor會自動啟動和停止所有其他Image Serving元件。

[SupervisorRegistry.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6)
