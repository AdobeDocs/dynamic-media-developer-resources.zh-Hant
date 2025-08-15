---
title: 暈映大小限制
description: 「影像演算」會對非金字塔暈映強制實行200萬畫素大小限制。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 69116b7f-45c0-42ed-9114-d01db3ce16be
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 0%

---

# 暈映大小限制{#vignette-size-limitation}

「影像演算」會對非金字塔暈映強制實行200萬畫素大小限制。

如果您的應用程式需要支援影像區域（寬度x高度）大於此限制的非金字塔暈映，請修改[！DNL `IrMaxNonPyrVignetteSize` /ImageServing/conf /ImageServerRegistry.conf]中&#x200B;*[!DNL install_root]*&#x200B;的值。

>[!NOTE]
>
>調整屬性`attribute::MaxPix`和`IS::MaxMessageSize`以允許異常大的回應影像大小。 如需詳細資訊，請參閱影像伺服檔案。
