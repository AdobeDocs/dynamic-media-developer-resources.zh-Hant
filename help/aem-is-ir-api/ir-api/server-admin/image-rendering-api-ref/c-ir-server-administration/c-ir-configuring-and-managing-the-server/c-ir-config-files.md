---
description: 影像呈現配置設定儲存在 [!DNL Platform Server] 配置檔案。
solution: Experience Manager
title: 配置檔案
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 44ffebae-4933-455b-a902-4f6e7bb69184
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# 配置檔案{#configuration-files}

影像呈現配置設定儲存在 [!DNL Platform Server] 配置檔案。

平台伺服器配置檔案位於[!DNL] *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]。 此檔案是JAVA屬性檔案。 必須注意遵守適當的公約，否則 [!DNL Platform Server] 可能無法啟動。 雙反斜線(`\\`)或在Windows檔案路徑中必須使用單個正斜槓(/)，而不是簡單反斜槓(\)，因為反斜槓在此類檔案中用作轉義字元。 檔案包含未記錄的屬性，這些屬性用於內部伺服器，不得修改。

請參閱 [配置設定參考](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81) 的子菜單。
