---
description: 影像目錄是用來將影像和支援資料（例如字型和ICC設定檔）的相關資訊提供給伺服器。
solution: Experience Manager
title: 概述
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 36cdd833-6fcb-4be6-a4f8-ba8d20580f29
TQID: 'https://experienceleague.adobe.com/RFHaFaMFjOo2Igk-pQRXrQSCtSMmVCWarO6wu0mv4g8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 275
ht-degree: 0%

---

# 概述{#overview}

影像目錄是用來將影像和支援資料（例如字型和ICC設定檔）的相關資訊提供給伺服器。

影像目錄是用來將影像和支援資料（例如字型和ICC設定檔）的相關資訊提供給伺服器。

每個影像目錄都包含必要的目錄屬性檔案和一組選用的目錄資料檔案：

* 影像資料檔案，可逐項列出影像和範本及其關聯的中繼資料。
* SVG資料檔案，其中詳細列示SVG檔案及其相關中繼資料。
* 巨集定義檔案，提供要求巨集的定義。
* 追蹤文字字型的字型對應檔案。
* 設定檔對映檔案，其中列舉ICC色彩設定檔。
* 規則集檔案，定義HTTP要求前置處理規則。

目錄資料檔案會依據目錄屬性檔案中的檔案參照，與影像目錄相關聯。 多個影像目錄可以共用相同的目錄資料檔案。

目錄屬性檔案必須有[!DNL .ini]檔案字尾，而且必須位於[!DNL Platform Server]的目錄資料夾( `PlatformServer::catalog.rootPath`)。 目錄資料檔案可以位於相同的資料夾或[!DNL Platform Server]可存取的任何其他資料夾中。

本檔案說明Dynamic Media影像伺服系統的影像目錄檔案格式。 目標對象是經驗豐富的程式設計師和網站開發人員，他們想要將Dynamic Media影像伺服用於網頁或自訂應用程式。

我們假設讀者通常熟悉Dynamic Media影像伺服系統、一般HTTP通訊協定標準和慣例，以及基本影像術語。
