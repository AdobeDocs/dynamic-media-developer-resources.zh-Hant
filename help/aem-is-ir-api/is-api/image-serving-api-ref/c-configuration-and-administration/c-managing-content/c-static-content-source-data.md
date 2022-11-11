---
description: 靜態內容源資料檔案僅由 [!DNL Platform Server].
solution: Experience Manager
title: 靜態內容來源資料
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3cf01fc2-c925-4039-8e03-cb909cca6a51
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---

# 靜態內容來源資料{#static-content-source-data}

靜態內容源資料檔案僅由 [!DNL Platform Server].

靜態內容資料檔案的路徑解析如下：

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

伺服器會從右到左組合路徑段，直到建立絕對檔案路徑為止。

全部 ` *[!DNL rootPath]*` 區段可以是空、相對或絕對路徑區段。

` *[!DNL catalogPath]*` 是絕對或相對檔案路徑/名稱。 *[!DNL requestPath]* 必須是相對檔案路徑/名稱。

多個 `PS::staticContent.rootPaths` 值可在中定義 [!DNL PlatformServer.conf]. 這允許源資料檔案跨多個檔案系統分發。 此 [!DNL Platform Server] 將按指定順序嘗試替代路徑，直到找到資料檔案為止。
