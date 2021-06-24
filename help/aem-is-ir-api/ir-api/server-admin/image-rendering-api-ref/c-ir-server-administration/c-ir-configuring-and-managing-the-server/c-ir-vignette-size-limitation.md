---
description: 影像呈現可強制對非金字塔暈映設定兩百萬像素大小限制。
solution: Experience Manager
title: 暈映大小限制
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 69116b7f-45c0-42ed-9114-d01db3ce16be
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---

# 暈映大小限制{#vignette-size-limitation}

影像呈現可強制對非金字塔暈映設定兩百萬像素大小限制。

如果您的應用程式需要支援影像區域（寬x高）大於此限制的非金字塔暈映，請修改[!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf]中`IrMaxNonPyrVignetteSize`的值。

>[!NOTE]
>
>`attribute::MaxPix` 和 `IS::MaxMessageSize` 可能也需要調整，以允許異常大的回應影像大小。如需詳細資訊，請參閱影像伺服檔案。
