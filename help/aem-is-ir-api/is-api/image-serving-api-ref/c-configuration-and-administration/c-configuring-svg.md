---
description: SvgRender元件是獨立的Java應用程式。
solution: Experience Manager
title: 配置SVG
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9013e13f-818f-41b4-80b6-2615d9a8742f
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 3%

---

# 配置SVG{#configuring-svg}

SvgRender元件是獨立的Java應用程式。

SVG配置設定位於 [!DNL PlatformServer.conf]。 [!DNL SVG.conf]。 [!DNL ImageServerRegistry.xml], [!DNL ServerSupervisorRegistry.xml]。

套接字連接用於在SvgRender和影像伺服器之間通信。 埠號為27346。 如有必要，可通過設定 `SVGRender.port` 在 [!DNL svg.conf] 和 `<SVGTcpPort>` 在 [!DNL ImageServerRegistry.xml] 的雙曲餘切值。

## 另請參閱 {#section-c085b47d54d44059bdaa67fd5e226e91}

[SVG配置設定](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
