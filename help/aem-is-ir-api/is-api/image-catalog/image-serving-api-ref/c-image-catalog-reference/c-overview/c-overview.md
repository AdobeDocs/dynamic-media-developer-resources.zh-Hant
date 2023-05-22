---
description: 影像目錄用於向伺服器提供關於影像和支援資料（如字型和ICC配置檔案）的資訊。
solution: Experience Manager
title: 概述
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 36cdd833-6fcb-4be6-a4f8-ba8d20580f29
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---

# 概述{#overview}

影像目錄用於向伺服器提供關於影像和支援資料（如字型和ICC配置檔案）的資訊。

影像目錄用於向伺服器提供關於影像和支援資料（如字型和ICC配置檔案）的資訊。

每個影像目錄都包含所需的目錄屬性檔案和一組可選目錄資料檔案：

* 影像資料檔案，它列出影像和模板及其相關元資料。
* SVG資料檔案，它列出SVG檔案及其關聯元資料。
* 宏定義檔案，它提供請求宏的定義。
* 字型映射檔案，用於跟蹤文本字型。
* 配置檔案映射檔案，它列出ICC顏色配置檔案。
* 規則集檔案，它定義HTTP請求預處理規則。

目錄資料檔案通過目錄屬性檔案中的檔案引用與影像目錄相關聯。 同一目錄資料檔案可由多個映像目錄共用。

目錄屬性檔案必須具有 [!DNL .ini] 檔案尾碼，必須位於 [!DNL Platform Server]&#39;s目錄資料夾( `PlatformServer::catalog.rootPath`)。 目錄資料檔案可以位於同一資料夾中，也可以位於 [!DNL Platform Server]。

本文檔介紹Dynamic Media影像服務系統的影像目錄檔案格式。 目標受眾是經驗豐富的程式設計師和網站開發人員，他們希望利用Dynamic Media影像服務為Web或自定義應用程式提供服務。

假定讀者通常熟悉Dynamic Media影像服務系統、一般HTTP協定標準和慣例以及基本的影像術語。
