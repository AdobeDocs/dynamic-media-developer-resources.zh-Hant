---
description: SvgRender元件是獨立的Java應用程式。
solution: Experience Manager
title: 設定SVG
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9013e13f-818f-41b4-80b6-2615d9a8742f
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 3%

---

# 設定SVG{#configuring-svg}

SvgRender元件是獨立的Java應用程式。

SVG組態設定位於[!DNL PlatformServer.conf]、[!DNL SVG.conf]、[!DNL ImageServerRegistry.xml]和[!DNL ServerSupervisorRegistry.xml]。

通訊端連線是用來在SvgRender和影像伺服器之間通訊。 連線埠號碼為27346。 如有必要，可透過將[!DNL svg.conf]中的`SVGRender.port`和[!DNL ImageServerRegistry.xml]中的`<SVGTcpPort>`設定為新值來變更它。

## 另請參閱 {#section-c085b47d54d44059bdaa67fd5e226e91}

[SVG組態設定](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
