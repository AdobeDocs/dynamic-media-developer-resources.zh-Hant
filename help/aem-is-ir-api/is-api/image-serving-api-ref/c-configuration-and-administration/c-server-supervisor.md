---
description: 映像服務元件由伺服器監視程式管理，該伺服器監視程式是Linux守護程式或Windows服務(S7Supervisor.exe，在「服務」控制面板中列為「Dynamic Media映像服務」)。
solution: Experience Manager
title: 伺服器主管
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---


# 伺服器主管{#server-supervisor}

映像服務元件由伺服器監視程式管理，該伺服器監視程式是Linux守護程式或Windows服務(S7Supervisor.exe，在「服務」控制面板中列為「Dynamic Media映像服務」)。

除了啟動和停止其他映像服務元件外，伺服器主管還負責確保這些元件的運行狀況。 如果元件發生崩潰，則會自動重新啟動它，以最大限度地減少任何服務中斷。

## 啟動和停止{#section-061d28d74e034a30adc39ea3e2031cd0}

使用Image Serving實用程式指令碼啟動、停止和重新啟動伺服器管理器。 如需詳細資訊，請參閱[公用程式檔案](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)。

啟動和停止Server Supervisor會自動啟動和停止所有其他Image Serving元件。

[SupervisorRegistry.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6)
