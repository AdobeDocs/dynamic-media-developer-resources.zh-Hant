---
description: 材料目錄提供許多「影像呈現」配置設定。
solution: Experience Manager
title: 材料目錄
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: c0b030b7-bcfb-4e6d-b74a-4533bdb801bf
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 0%

---

# 材料目錄{#material-catalogs}

材料目錄提供許多「影像呈現」配置設定。

物料目錄可將請求中使用的暈映和物料ID映射到實際的檔案路徑，可以儲存與物料相關的所有元資料，並為模板提供容器。 它們跟蹤ICC配置檔案和命令宏。

只有影像呈現的Java元件（與Platform伺服器共同位置）才能存取材料目錄。 目錄屬性檔案必須有[!DNL .ini]尾碼，並放置在已註冊的目錄資料夾([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7))中。 預設物料目錄([!DNL default.ini])必須始終存在，並且必須填入所有屬性，才能正確運行「影像伺服」。
