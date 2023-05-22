---
description: 將這些伺服器設定用於內容資料資料夾。
solution: Experience Manager
title: 內容資料資料夾
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9aa4121f-25f8-49d0-a304-7ae756c046f5
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# 內容資料資料夾{#content-data-folders}

將這些伺服器設定用於內容資料資料夾。

## IS::RootPath — 映像資料根資料夾 {#section-5c57569514bb4d00b19de31d2e137e3b}

所有源資料（包括影像、字型和ICC配置檔案）的位置。 這可以是一個或多個相對於 *[!DNL install_folder]*，用分號分隔。 如果空， *[!DNL install_folder]* 是預設根目錄。 可以指定多個值以在多個檔案系統中分發影像資料。 映像伺服器將按指定的順序嘗試根路徑，直到找到所請求的檔案。

## PS::staticContent.rootPath — 靜態內容資料根資料夾 {#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

要通過 [!DNL /is/static] 上下文。 可以是一個或多個相對於 *[!DNL install_folder]*，用分號分隔。 如果空， *[!DNL install_folder]* 是預設根目錄。

可以指定多個值並用分號分隔，以在多個檔案系統中分發靜態內容。 通常設定為與 `IS::RootPath`。

的 [!DNL Platform Server] 嘗試根路徑的順序，直到找到所請求的檔案。

>[!NOTE]
>
>預設情況下，此欄位被有意設定為不存在的位置([!DNL) *[!DNL install_folder]*/static])，有效禁用靜態內容服務。

## IS::SaveDirectory — 檔案保存根資料夾 {#section-1c517f8d49ce4cb8b9013e520bf309c9}

的根路徑 `attribute::SavePath` （使用者） `req=saveToFile`)。 映像伺服器必須具有為其建立映像檔案的子資料夾的建立訪問權限。
