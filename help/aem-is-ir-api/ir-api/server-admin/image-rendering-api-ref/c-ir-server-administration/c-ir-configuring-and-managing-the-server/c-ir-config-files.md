---
description: 影像呈現配置設定儲存在Platform Server配置檔案中。
solution: Experience Manager
title: 組態檔
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: 44ffebae-4933-455b-a902-4f6e7bb69184
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# 組態檔{#configuration-files}

影像呈現配置設定儲存在Platform Server配置檔案中。

平台伺服器配置檔案位於[!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]。 此檔案是JAVA屬性檔案。 請務必遵循適當的慣例，否則Platform伺服器可能無法啟動。 在Windows檔案路徑中，必須使用雙反斜線(`\\`)或單正斜線(/)，而不是使用簡單反斜線(\)，因為反斜線在此類型檔案中被用作逸出字元。 該檔案包含未記錄的屬性，這些屬性供內部伺服器使用，不得修改。

如需所有影像呈現組態設定的清單，請參閱[組態設定參考](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81) 。
