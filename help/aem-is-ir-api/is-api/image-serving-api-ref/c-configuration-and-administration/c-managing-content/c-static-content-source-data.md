---
description: 靜態內容源資料檔案僅由Platform Server訪問。
solution: Experience Manager
title: 靜態內容來源資料
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: 3cf01fc2-c925-4039-8e03-cb909cca6a51
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# 靜態內容來源資料{#static-content-source-data}

靜態內容源資料檔案僅由Platform Server訪問。

靜態內容資料檔案的路徑解析如下：

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

伺服器會從右到左組合路徑段，直到建立絕對檔案路徑為止。

所有` *[!DNL rootPath]*`區段都可以是空白、相對或絕對路徑區段。

` *[!DNL catalogPath]*` 是絕對或相對檔案路徑/名稱。*[!DNL requestPath]* 必須是相對檔案路徑/名稱。

可在[!DNL PlatformServer.conf]中定義多個`PS::staticContent.rootPaths`值。 這允許源資料檔案跨多個檔案系統分發。 Platform伺服器會按指定順序嘗試替代路徑，直到找到資料檔案為止。
