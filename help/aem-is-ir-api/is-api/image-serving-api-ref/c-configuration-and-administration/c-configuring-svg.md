---
description: SvgRender元件是獨立的Java應用程式。
solution: Experience Manager
title: 設定SVG
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 2%

---


# 配置SVG{#configuring-svg}

SvgRender元件是獨立的Java應用程式。

SVG配置設定位於[!DNL PlatformServer.conf]、[!DNL SVG.conf]、[!DNL ImageServerRegistry.xml]和[!DNL ServerSupervisorRegistry.xml]中。

套接字連接用於在SvgRender和影像伺服器之間通信。 埠號為27346。 如有必要，可將[!DNL svg.conf]中的`SVGRender.port`和[!DNL ImageServerRegistry.xml]中的`<SVGTcpPort>`設為新值。

## 另請參閱 {#section-c085b47d54d44059bdaa67fd5e226e91}

[SVG配置設定](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
