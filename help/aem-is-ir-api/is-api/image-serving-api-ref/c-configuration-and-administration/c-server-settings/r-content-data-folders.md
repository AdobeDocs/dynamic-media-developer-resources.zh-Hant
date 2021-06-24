---
description: 對內容資料夾使用這些伺服器設定。
solution: Experience Manager
title: 內容資料夾
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 9aa4121f-25f8-49d0-a304-7ae756c046f5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 0%

---

# 內容資料夾{#content-data-folders}

對內容資料夾使用這些伺服器設定。

## IS::RootPath — 影像資料根資料夾 {#section-5c57569514bb4d00b19de31d2e137e3b}

所有源資料的位置，包括影像、字型和ICC配置檔案。 這可以是相對於&#x200B;*[!DNL install_folder]*&#x200B;的一個或多個絕對檔案路徑或路徑，用分號分隔。 如果為空，*[!DNL install_folder]*&#x200B;為預設根。 可以指定多個值，以跨多個檔案系統分發影像資料。 映像伺服器將按指定順序嘗試根路徑，直到找到所請求的檔案。

## PS::staticContent.rootPath — 靜態內容資料根資料夾 {#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

要透過[!DNL /is/static]內容傳送的靜態內容來源資料的位置。 可以是相對於&#x200B;*[!DNL install_folder]*&#x200B;的一個或多個絕對檔案路徑或路徑，用分號分隔。 如果為空，*[!DNL install_folder]*&#x200B;為預設根。

可以指定多個值（用分號分隔）以跨多個檔案系統分發靜態內容。 通常設為與`IS::RootPath`相同的值。

Platform伺服器會按指定的順序嘗試根路徑，直到找到請求的檔案為止。

>[!NOTE]
>
>依預設，此欄位會刻意設為非現有位置([!DNL *[!DNL install_folder]*/static])，以有效停用靜態內容服務。

## IS::SaveDirectory — 檔案保存根資料夾 {#section-1c517f8d49ce4cb8b9013e520bf309c9}

`attribute::SavePath`的根路徑（由`req=saveToFile`使用）。 影像伺服器必須具有建立影像檔案的子資料夾的建立存取權限。
