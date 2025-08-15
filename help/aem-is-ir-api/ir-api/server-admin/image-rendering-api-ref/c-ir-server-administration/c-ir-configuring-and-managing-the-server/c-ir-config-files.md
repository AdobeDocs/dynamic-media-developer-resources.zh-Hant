---
description: 影像演算組態設定儲存在 [!DNL Platform Server] 組態檔中。
solution: Experience Manager
title: 組態檔
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 44ffebae-4933-455b-a902-4f6e7bb69184
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# 組態檔{#configuration-files}

影像演算組態設定儲存在[!DNL Platform Server]組態檔中。

平台伺服器設定檔位於[!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]。 此檔案是JAVA屬性檔案。 請務必遵循適當的慣例，否則[!DNL Platform Server]可能無法啟動。 在Windows檔案路徑中，必須使用雙反斜線(`\\`)或單正斜線(/)，而非簡單反斜線(\)，因為反斜線會作為此型別檔案的逸出字元。 檔案包含未記錄的屬性，這些屬性供內部伺服器使用，且不得修改。

如需所有影像演算組態設定的清單，請參閱[組態設定參考](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81)。
