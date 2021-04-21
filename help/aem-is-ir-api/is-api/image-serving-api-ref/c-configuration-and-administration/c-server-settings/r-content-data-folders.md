---
description: 對內容資料檔案夾使用這些伺服器設定。
solution: Experience Manager
title: 內容資料夾
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---


# 內容資料資料夾{#content-data-folders}

對內容資料檔案夾使用這些伺服器設定。

## IS::RootPath —— 映像資料根資料夾{#section-5c57569514bb4d00b19de31d2e137e3b}

所有來源資料的位置，包括影像、字型和ICC描述檔。 這可以是相對於&#x200B;*[!DNL install_folder]*&#x200B;的一個或多個絕對檔案路徑或路徑，以分號分隔。 如果為空，則&#x200B;*[!DNL install_folder]*&#x200B;是預設根。 可指定多個值，以在多個檔案系統間散發影像資料。 影像伺服器會依指定順序嘗試根路徑，直到找到請求的檔案。

## PS::staticContent.rootPath —— 靜態內容資料根資料夾{#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

要透過[!DNL /is/static]內容傳送的靜態內容來源資料的位置。 可以是相對於&#x200B;*[!DNL install_folder]*&#x200B;的一個或多個絕對檔案路徑或路徑，以分號分隔。 如果為空，則&#x200B;*[!DNL install_folder]*&#x200B;是預設根。

多個值可以用分號指定——分隔——以在多個檔案系統間分發靜態內容。 通常設定為與`IS::RootPath`相同的值。

平台伺服器會按照指定的順序嘗試根路徑，直到找到所請求的檔案。

>[!NOTE]
>
>預設情況下，此欄位被有意設定為非現有位置([!DNL *[!DNL install_folder]*/static])，從而有效地禁用靜態內容服務。

## IS::SaveDirectory —— 檔案保存根資料夾{#section-1c517f8d49ce4cb8b9013e520bf309c9}

`attribute::SavePath`的根路徑（由`req=saveToFile`使用）。 影像伺服器必須擁有建立影像檔案的子資料夾存取權限。
