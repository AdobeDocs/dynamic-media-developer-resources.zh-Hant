---
description: 靜態內容來源資料檔案僅由平台伺服器存取。
seo-description: 靜態內容來源資料檔案僅由平台伺服器存取。
seo-title: 靜態內容來源資料
solution: Experience Manager
title: 靜態內容來源資料
topic: Scene7 Image Serving - Image Rendering API
uuid: a3280ce7-20d7-4f4b-bf3e-e77cc7aca35f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 靜態內容來源資料{#static-content-source-data}

靜態內容來源資料檔案僅由平台伺服器存取。

靜態內容資料檔案的路徑解析如下：

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

伺服器會從右至左組合路徑區段，直到建立絕對檔案路徑為止。

所有 ` *[!DNL rootPath]*` 區段都可以是空、相對或絕對路徑區段。

` *[!DNL catalogPath]*` 是絕對或相對檔案路徑／名稱。 *[!DNL requestPath]* 必須是相對檔案路徑／名稱。

可在 `PS::staticContent.rootPaths` 中定義多個值 [!DNL PlatformServer.conf]。 這允許源資料檔案跨多個檔案系統分發。 平台伺服器會依指定順序嘗試替代路徑，直到找到資料檔案為止。
