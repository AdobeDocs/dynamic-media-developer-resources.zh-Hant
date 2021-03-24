---
description: 靜態內容來源資料檔案僅由平台伺服器存取。
solution: Experience Manager
title: 靜態內容來源資料
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員、商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---


# 靜態內容來源資料{#static-content-source-data}

靜態內容來源資料檔案僅由平台伺服器存取。

靜態內容資料檔案的路徑解析如下：

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

伺服器會從右至左組合路徑區段，直到建立絕對檔案路徑為止。

所有` *[!DNL rootPath]*`區段皆可為空、相對或絕對路徑區段。

` *[!DNL catalogPath]*` 是絕對或相對檔案路徑／名稱。*[!DNL requestPath]* 必須是相對檔案路徑／名稱。

在[!DNL PlatformServer.conf]中可定義多個`PS::staticContent.rootPaths`值。 這允許源資料檔案跨多個檔案系統分發。 平台伺服器會依指定順序嘗試替代路徑，直到找到資料檔案為止。
