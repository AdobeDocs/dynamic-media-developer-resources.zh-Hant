---
description: 影像演算對非金字塔暈映強制執行200萬像素大小限制。
seo-description: 影像演算對非金字塔暈映強制執行200萬像素大小限制。
seo-title: 暈映大小限制
solution: Experience Manager
title: 暈映大小限制
topic: Scene7 Image Serving - Image Rendering API
uuid: 218e8c7e-f313-47cb-af42-30c585d4ec12
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 暈映大小限制{#vignette-size-limitation}

影像演算對非金字塔暈映強制執行200萬像素大小限制。

如果您的應用 `IrMaxNonPyrVignetteSize` 程式需要支援影像區域（寬x高度）大於此限制的非金字塔暈映，請修改[!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf]中的值。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>`attribute::MaxPix` 而且 `IS::MaxMessageSize` 可能也需要調整，以允許異常大的回應影像大小。 如需詳細資訊，請參閱影像伺服檔案。

