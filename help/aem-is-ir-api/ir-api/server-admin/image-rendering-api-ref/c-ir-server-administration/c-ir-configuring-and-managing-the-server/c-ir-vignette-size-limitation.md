---
title: 暈映大小限制
description: 「影像演算」會對非金字塔暈映強制實行200萬畫素大小限制。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 69116b7f-45c0-42ed-9114-d01db3ce16be
TQID: 'https://experienceleague.adobe.com/qPrnkvYXinvZAfx-s6ePjpe64qsoBfwtVbUJ-fYBbmc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 78
ht-degree: 0%

---

# 暈映大小限制{#vignette-size-limitation}

「影像演算」會對非金字塔暈映強制實行200萬畫素大小限制。

如果您的應用程式需要支援影像區域（寬度x高度）大於此限制的非金字塔暈映，請修改[！DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf]中`IrMaxNonPyrVignetteSize`的值。

>[!NOTE]
>
>調整屬性`attribute::MaxPix`和`IS::MaxMessageSize`以允許異常大的回應影像大小。 如需詳細資訊，請參閱影像伺服檔案。

