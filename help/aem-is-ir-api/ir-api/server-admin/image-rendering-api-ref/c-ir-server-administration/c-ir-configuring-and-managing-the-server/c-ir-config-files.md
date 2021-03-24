---
description: 映像渲染配置設定儲存在平台伺服器配置檔案中。
solution: Experience Manager
title: 配置檔案
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員、商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---


# 配置檔案{#configuration-files}

映像渲染配置設定儲存在平台伺服器配置檔案中。

平台伺服器配置檔案位於[!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]。 此檔案是JAVA屬性檔案。 必須小心，以遵循適當的慣例，否則平台伺服器可能無法啟動。 在Windows檔案路徑中，必須使用雙反斜線(`\\`)或單正斜線(/)，而非簡單反斜線(\)，因為反斜線是此類檔案中的轉義字元。 該檔案包含未記錄的屬性，這些屬性供內部伺服器使用，不得修改。

請參閱[組態設定參考](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81)，以取得所有影像演算組態設定的清單。
