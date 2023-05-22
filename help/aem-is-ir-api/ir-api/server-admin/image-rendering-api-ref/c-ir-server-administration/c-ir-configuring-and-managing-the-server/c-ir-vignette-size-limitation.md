---
description: 影像渲染強制對非稜錐影像實施200萬像素大小限制。
solution: Experience Manager
title: Vignette大小限制
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 69116b7f-45c0-42ed-9114-d01db3ce16be
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 0%

---

# Vignette大小限制{#vignette-size-limitation}

影像渲染強制對非稜錐影像實施200萬像素大小限制。

修改 `IrMaxNonPyrVignetteSize` 在[!DNL中 *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf]如果您的應用程式需要支援影像區域（寬度x高度）大於此限制的非稜錐圖。

>[!NOTE]
>
>`attribute::MaxPix` 和 `IS::MaxMessageSize` 可能還需要調整以允許異常大的響應影像大小。 有關詳細資訊，請參閱「Image Serving（影像服務）」文檔。
