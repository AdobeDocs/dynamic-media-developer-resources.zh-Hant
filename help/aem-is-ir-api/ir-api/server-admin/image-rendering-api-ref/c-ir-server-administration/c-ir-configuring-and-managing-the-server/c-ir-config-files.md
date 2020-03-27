---
description: 映像渲染配置設定儲存在平台伺服器配置檔案中。
seo-description: 映像渲染配置設定儲存在平台伺服器配置檔案中。
seo-title: 配置檔案
solution: Experience Manager
title: 配置檔案
topic: Scene7 Image Serving - Image Rendering API
uuid: ffd1c65b-e084-4a7e-9a15-600d6c5b173a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 配置檔案{#configuration-files}

映像渲染配置設定儲存在平台伺服器配置檔案中。

平台伺服器配置檔案位於[!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]。 此檔案是JAVA屬性檔案。 必須小心，以遵循適當的慣例，否則平台伺服器可能無法啟動。 在Windows檔案路徑中，必須使用雙反斜線(\\)或單正斜線(/)，而非簡單反斜線(\)，因為反斜線用作此類檔案的轉義字元。 該檔案包含未記錄的屬性，這些屬性供內部伺服器使用，不得修改。

有關所有「圖 [像渲染」配置設定的清單](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81) ，請參閱配置設定參考。
