---
description: 對內容資料檔案夾使用這些伺服器設定。
seo-description: 對內容資料檔案夾使用這些伺服器設定。
seo-title: 內容資料夾
solution: Experience Manager
title: 內容資料夾
topic: Scene7 Image Serving - Image Rendering API
uuid: 7c4d60ca-8a8b-453c-887d-a6a16eacc883
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---


# 內容資料夾{#content-data-folders}

對內容資料檔案夾使用這些伺服器設定。

## IS::RootPath —— 映像資料根資料夾 {#section-5c57569514bb4d00b19de31d2e137e3b}

所有來源資料的位置，包括影像、字型和ICC描述檔。 這可以是一個或多個相對的絕對檔案路徑或路徑， *[!DNL install_folder]*&#x200B;以分號分隔。 如果為空， *[!DNL install_folder]* 則為預設根。 可指定多個值，以在多個檔案系統間散發影像資料。 影像伺服器會依指定順序嘗試根路徑，直到找到請求的檔案。

## PS::staticContent.rootPath —— 靜態內容資料根資料夾 {#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

靜態內容來源資料的位置，該位置擬透過內容傳 [!DNL /is/static] 送。 可以是一個或多個相對的絕對檔案路徑或路徑， *[!DNL install_folder]*&#x200B;以分號分隔。 如果為空， *[!DNL install_folder]* 則為預設根。

多個值可以用分號指定——分隔——以在多個檔案系統間分發靜態內容。 通常設為與相同的值 `IS::RootPath`。

平台伺服器會按照指定的順序嘗試根路徑，直到找到所請求的檔案。

>[!NOTE]
>
>預設情況下，此欄位被有意設定為非現有位置([!DNL *[!DNL install_folder]*/static])，從而有效地禁用靜態內容服務。

## IS::SaveDirectory —— 檔案保存根資料夾 {#section-1c517f8d49ce4cb8b9013e520bf309c9}

的根路 `attribute::SavePath` 徑(由 `req=saveToFile`使用)。 影像伺服器必須擁有建立影像檔案的子資料夾存取權限。
