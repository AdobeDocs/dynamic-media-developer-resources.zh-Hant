---
description: 只有 [!DNL Platform Server]可存取靜態內容來源資料檔。
solution: Experience Manager
title: 靜態內容來源資料
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3cf01fc2-c925-4039-8e03-cb909cca6a51
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---

# 靜態內容來源資料{#static-content-source-data}

只有[!DNL Platform Server]可存取靜態內容來源資料檔。

靜態內容資料檔案的路徑解析如下：

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

伺服器會由右至左組合路徑區段，直到建立絕對檔案路徑為止。

所有` *[!DNL rootPath]*`區段都可以是空白、相對或絕對路徑區段。

` *[!DNL catalogPath]*`是絕對或相對檔案路徑/名稱。 *[!DNL requestPath]*&#x200B;必須為相對檔案路徑/名稱。

可在`PS::staticContent.rootPaths`中定義多個[!DNL PlatformServer.conf]值。 如此一來，來源資料檔案便可以分散至多個檔案系統。 [!DNL Platform Server]會依指定的順序嘗試替代路徑，直到找到資料檔為止。
