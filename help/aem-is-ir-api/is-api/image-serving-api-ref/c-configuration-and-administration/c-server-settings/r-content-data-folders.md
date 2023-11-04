---
description: 對內容資料夾使用這些伺服器設定。
solution: Experience Manager
title: 內容資料夾
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9aa4121f-25f8-49d0-a304-7ae756c046f5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# 內容資料夾{#content-data-folders}

對內容資料夾使用這些伺服器設定。

## IS：：RootPath — 影像資料根資料夾 {#section-5c57569514bb4d00b19de31d2e137e3b}

所有來源資料（包括影像、字型和ICC設定檔）的位置。 這可以是一或多個絕對的檔案路徑或相對於 *[!DNL install_folder]*，以分號分隔。 如果空白， *[!DNL install_folder]* 是預設根目錄。 可以指定多個值，以將影像資料分散到多個檔案系統中。 影像伺服器會依指定的順序嘗試根路徑，直到找到要求的檔案為止。

## PS：：staticContent.rootPath — 靜態內容資料根資料夾 {#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

要透過以下方式傳送的靜態內容來源資料的位置 [!DNL /is/static] 內容。 可以是一個或多個絕對的檔案路徑或相對於 *[!DNL install_folder]*，以分號分隔。 如果空白， *[!DNL install_folder]* 是預設根目錄。

您可以指定多個值（以分號分隔），將靜態內容分散到多個檔案系統中。 通常會設定為與相同的值 `IS::RootPath`.

此 [!DNL Platform Server] 會依指定的順序嘗試根路徑，直到找到要求的檔案為止。

>[!NOTE]
>
>依預設，此欄位會刻意設定為不存在的位置( [！DNL *[!DNL install_folder]*/static])，有效停用靜態內容服務。

## IS：：SaveDirectory — 檔案儲存根資料夾 {#section-1c517f8d49ce4cb8b9013e520bf309c9}

的根路徑 `attribute::SavePath` (使用者： `req=saveToFile`)。 「影像伺服器」必須對其建立影像檔案的子資料夾具有建立存取許可權。
