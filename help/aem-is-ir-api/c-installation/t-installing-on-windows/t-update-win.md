---
title: 從IS 4.7.4或更高版本更新
description: 升級Dynamic Media映像服務時，請執行此過程。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0781f19-4aa8-46f7-a586-4724ff8a2e68
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# 從IS 4.7.4或更高版本更新{#updating-from-is-or-later}

升級Dynamic Media映像服務時，請執行此過程。

如果從較舊版本的映像服務升級，請聯繫支援人員以獲得正確的流程。

>[!NOTE]
>
>的 [!DNL webapps] 升級時可能會刪除資料夾。 備份 [!DNL webapps] 資料夾。

1. 使用管理權限登錄到伺服器主機。
1. 提取Image Service分發zip檔案的內容。
1. 通過運行啟動安裝嚮導 `setup/setup.exe`。
1. 選擇 **[!UICONTROL 下一個]** 要進入最終用戶許可協定(EULA)，請閱讀許可協定，然後選擇 **[!UICONTROL 是]**。

   下一頁顯示以前的配置設定。
1. 按一下 **[!UICONTROL 下一個]** 啟動更新安裝。

   >[!NOTE]
   >
   >安裝程式將舊伺服器配置檔案備份到 [!DNL BACKUP/] 的子菜單。

1. 安裝完成後，選擇 **[!UICONTROL 完成]** ，可退出安裝嚮導。

   有時，安裝嚮導可能會要求您重新啟動系統。

在更新期間， [!DNL ImageServing/conf/server.xml] 檔案更新為最新設定。 如果已更改或添加了任何值，則應保存現有值 [!DNL server.xml] 並在升級後重新實施更改。

在安裝更新後，請考慮在使伺服器生存之前預熱HTTP響應快取。 請參閱 `playlog` 的子菜單。
