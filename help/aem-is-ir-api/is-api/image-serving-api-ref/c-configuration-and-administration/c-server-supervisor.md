---
description: 映像伺服器元件由伺服器主管管理，伺服器主管是Linux守護程式或Windows服務(S7Supervisor.exe，在「服務控制面板」中列為「Dynamic Media映像伺服器」)。
solution: Experience Manager
title: 伺服器主管
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 83b6a63f-6bb8-4a14-b8d5-389d23fae57c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# 伺服器主管{#server-supervisor}

映像伺服器元件由伺服器主管管理，伺服器主管是Linux守護程式或Windows服務(S7Supervisor.exe，在「服務控制面板」中列為「Dynamic Media映像伺服器」)。

除了啟動和停止其他映像服務元件外，伺服器主管還負責確保這些其他元件的運行狀況。 如果元件當機，則會自動重新啟動，以將任何服務中斷降至最低。

## 啟動和停止 {#section-061d28d74e034a30adc39ea3e2031cd0}

使用映像服務實用程式指令碼啟動、停止和重新啟動伺服器主管。 有關詳細資訊，請參閱[實用程式文檔](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)。

啟動和停止伺服器主管會自動啟動和停止所有其他映像服務元件。

[SupervisorRegistry.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6)
