---
description: 影像目錄用於向伺服器提供關於影像和支援資料（如字型和ICC配置檔案）的資訊。
solution: Experience Manager
title: 概述
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 36cdd833-6fcb-4be6-a4f8-ba8d20580f29
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# 概述{#overview}

影像目錄用於向伺服器提供關於影像和支援資料（如字型和ICC配置檔案）的資訊。

影像目錄用於向伺服器提供關於影像和支援資料（如字型和ICC配置檔案）的資訊。

每個影像目錄都包含所需的目錄屬性檔案和一組可選目錄資料檔案：

* 影像資料檔案，列出影像和範本及其相關的中繼資料。
* SVG資料檔案，列出SVG檔案及其關聯的元資料。
* 宏定義檔案，提供請求宏的定義。
* 跟蹤文本字型的字型映射檔案。
* 配置檔案映射檔案，它列出ICC顏色配置檔案。
* 規則集檔案，定義HTTP要求前處理規則。

目錄資料檔案與目錄屬性檔案中的檔案引用關聯。 同一目錄資料檔案可由多個影像目錄共用。

目錄屬性檔案必須具有[!DNL .ini]檔案尾碼，且必須位於Platform Server的目錄資料夾(`PlatformServer::catalog.rootPath`)中。 目錄資料檔案可以位於Platform Server可存取的相同資料夾或任何其他資料夾中。

本檔案說明Dynamic Media影像伺服系統的影像目錄檔案格式。 目標對象是經驗豐富的程式設計師和網站開發人員，他們希望將Dynamic Media影像服務用於網頁或自訂應用程式。

假設讀者通常熟悉Dynamic Media影像伺服系統、一般HTTP通訊協定標準和慣例，以及基本影像術語。
