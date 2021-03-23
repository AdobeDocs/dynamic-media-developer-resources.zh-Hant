---
description: 影像演算對非金字塔暈映強制執行200萬像素大小限制。
seo-description: 影像演算對非金字塔暈映強制執行200萬像素大小限制。
seo-title: 暈映大小限制
solution: Experience Manager
title: 暈映大小限制
uuid: 218e8c7e-f313-47cb-af42-30c585d4ec12
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員、商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---


# 暈映大小限制{#vignette-size-limitation}

影像演算對非金字塔暈映強制執行200萬像素大小限制。

如果您的應用程式需要支援影像區域（寬x高度）大於此限制的非金字塔暈映，請修改[!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf]中`IrMaxNonPyrVignetteSize`的值。

>[!NOTE]
>
>`attribute::MaxPix` 而且 `IS::MaxMessageSize` 可能需要調整，以允許異常大的回應影像大小。如需詳細資訊，請參閱影像伺服檔案。

