---
description: SvgRender元件是獨立的Java應用程式。
solution: Experience Manager
title: 配置SVG
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 9013e13f-818f-41b4-80b6-2615d9a8742f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 2%

---

# 配置SVG{#configuring-svg}

SvgRender元件是獨立的Java應用程式。

SVG配置設定位於[!DNL PlatformServer.conf]、[!DNL SVG.conf]、[!DNL ImageServerRegistry.xml]和[!DNL ServerSupervisorRegistry.xml]中。

套接字連接用於在SvgRender和影像伺服器之間通信。 埠號是27346。 如有必要，可將[!DNL svg.conf]中的`SVGRender.port`和[!DNL ImageServerRegistry.xml]中的`<SVGTcpPort>`設定為新值來變更。

## 另請參閱 {#section-c085b47d54d44059bdaa67fd5e226e91}

[SVG配置設定](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
