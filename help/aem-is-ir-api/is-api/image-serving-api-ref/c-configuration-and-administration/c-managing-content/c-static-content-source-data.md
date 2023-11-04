---
description: 靜態內容來源資料檔案只能由以下使用者存取： [!DNL Platform Server].
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

靜態內容來源資料檔案只能由以下使用者存取： [!DNL Platform Server].

靜態內容資料檔案的路徑解析如下：

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

伺服器會由右至左組合路徑區段，直到建立絕對檔案路徑為止。

全部 ` *[!DNL rootPath]*` 區段可以是空白、相對或絕對路徑區段。

` *[!DNL catalogPath]*` 是絕對或相對檔案路徑/名稱。 *[!DNL requestPath]* 必須為相對檔案路徑/名稱。

多個 `PS::staticContent.rootPaths` 值可在以下位置定義： [!DNL PlatformServer.conf]. 如此一來，來源資料檔案便可以分散至多個檔案系統。 此 [!DNL Platform Server] 會以指定的順序嘗試替代路徑，直到找到資料檔案為止。
