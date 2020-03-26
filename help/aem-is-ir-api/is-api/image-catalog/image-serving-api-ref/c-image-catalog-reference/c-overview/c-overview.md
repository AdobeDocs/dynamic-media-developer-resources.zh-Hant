---
description: 影像目錄可用來提供影像和支援資料（例如字型和ICC描述檔）的相關資訊給伺服器。
seo-description: 影像目錄可用來提供影像和支援資料（例如字型和ICC描述檔）的相關資訊給伺服器。
seo-title: 概述
solution: Experience Manager
title: 概述
topic: Scene7 Image Serving - Image Rendering API
uuid: e8c0401b-9161-4624-babb-6c7afb443e65
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 綜覽{#overview}

影像目錄可用來提供影像和支援資料（例如字型和ICC描述檔）的相關資訊給伺服器。

影像目錄可用來提供影像和支援資料（例如字型和ICC描述檔）的相關資訊給伺服器。

每個影像目錄都包含必要的目錄屬性檔案和一組選用的目錄資料檔案：

* 影像資料檔案，列出影像和範本及其相關的中繼資料。
* SVG資料檔案，列出SVG檔案及其相關的中繼資料。
* 宏定義檔案，提供請求宏的定義。
* 字型對應檔案，可追蹤文字字型。
* 描述檔映射檔案，列出ICC色彩描述檔。
* 規則集檔案，用來定義HTTP要求前處理規則。

目錄資料檔案通過目錄屬性檔案中的檔案引用與影像目錄相關聯。 同一個目錄資料檔案可由多個影像目錄共用。

目錄屬性檔案必須 [!DNL .ini] 有檔案尾碼，並且必須位於平台伺服器的目錄資料夾( `PlatformServer::catalog.rootPath`)中。 目錄資料檔案可位於平台伺服器可存取的相同資料夾或任何其他資料夾中。

本檔案說明Scene7 Image Serving系統的Image Catalog檔案格式。 目標受眾是經驗豐富的程式設計人員和網站開發人員，他們希望將Scene7 Image Serving運用於網頁或自訂應用程式。

假設讀者通常熟悉Scene7 Image Serving系統、一般HTTP通訊協定標準和慣例，以及基本的影像術語。
