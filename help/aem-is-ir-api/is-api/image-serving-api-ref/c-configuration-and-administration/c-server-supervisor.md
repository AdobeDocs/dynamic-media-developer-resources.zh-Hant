---
description: 映像服務元件由伺服器主管管理，伺服器主管是Linux守護程式或Windows服務(S7Supervisor.exe，在「服務」控制面板中列為「Dynamic Media映像服務」)。
solution: Experience Manager
title: 伺服器主管
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 83b6a63f-6bb8-4a14-b8d5-389d23fae57c
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---

# 伺服器主管{#server-supervisor}

映像服務元件由伺服器主管管理，伺服器主管是Linux守護程式或Windows服務(S7Supervisor.exe，在「服務」控制面板中列為「Dynamic Media映像服務」)。

除了啟動和停止其他映像服務元件外，伺服器主管還負責確保這些其他元件的運行狀況。 如果元件崩潰，將自動重新啟動它以最小化任何服務中斷。

## 啟動和停止 {#section-061d28d74e034a30adc39ea3e2031cd0}

伺服器監控器已使用映像服務實用程式指令碼啟動、停止和重新啟動。 查看 [實用程式文檔](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f) 的子菜單。

啟動和停止伺服器主管將自動啟動和停止所有其他映像服務元件。

[SupervisorRegistry.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6)
