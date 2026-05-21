---
description: SvgRender元件是獨立的Java應用程式。
solution: Experience Manager
title: 設定SVG
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9013e13f-818f-41b4-80b6-2615d9a8742f
TQID: 'https://experienceleague.adobe.com/e6eoh1OQJoWFv0-C1xQTqygrGY4Z7m6IkefFblj-yuE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 65
ht-degree: 3%

---

# 設定SVG{#configuring-svg}

SvgRender元件是獨立的Java應用程式。

SVG組態設定位於[!DNL PlatformServer.conf]、[!DNL SVG.conf]、[!DNL ImageServerRegistry.xml]和[!DNL ServerSupervisorRegistry.xml]。

通訊端連線是用來在SvgRender和影像伺服器之間通訊。 連線埠號碼為27346。 如有必要，可透過將[!DNL svg.conf]中的`SVGRender.port`和[!DNL ImageServerRegistry.xml]中的`<SVGTcpPort>`設定為新值來變更它。

## 另請參閱 {#section-c085b47d54d44059bdaa67fd5e226e91}

[SVG組態設定](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
