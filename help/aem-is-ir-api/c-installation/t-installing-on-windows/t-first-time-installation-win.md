---
description: 使用這些步驟在Windows上首次安裝映像服務。
solution: Experience Manager
title: 首次安裝
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4e34d78c-1b5b-45cf-acc5-ff12cbc6ed01
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 0%

---

# 首次安裝{#installing-for-the-first-time}

使用這些步驟在Windows上首次安裝映像服務。

1. 以管理權限登入您的伺服器主機。
1. 如果您已收到許可證，請將其複製到伺服器，然後按兩下該檔案運行許可證安裝。

   如果您尚未獲得許可證，則可以繼續安裝，並稍後安裝該許可證。
1. 解壓縮Image Serving分送Zip檔案的內容。
1. 運行[!DNL setup]/ [!DNL setup.exe]以啟動安裝嚮導。
1. 按一下「下一步」以前往「最終用戶許可協定」(EULA)，閱讀許可協定，然後按一下「**[!UICONTROL Yes]**」。

   「[!DNL Authentication]」對話框隨即顯示。
1. 如果已安裝許可證，並且許可證資訊顯示在[!DNL Authentication]對話框中，按一下&#x200B;**[!UICONTROL Next]**&#x200B;繼續。

   如果您沒有許可證，請按一下「請求許可證」****。 下一個對話框顯示您電腦的網路介面卡MAC地址之一。 以電子郵件傳送此MAC地址、您的公司名稱，以及您要安裝的產品，如提示所指示。

   **重要：** 此許可證基於此主機上安裝的其中一個網路介面卡的MAC地址。如果禁用、刪除或更換此卡，則不再將許可證識別為有效。 請務必取得要用於IS的硬體配置的許可證。

   您可以繼續安裝IS（沒有有效的許可證），然後安裝該許可證。 若要繼續，請按一下&#x200B;**[!UICONTROL Back]**&#x200B;返回[!DNL Authentication]對話框，然後按一下&#x200B;**[!UICONTROL Next]**。
1. 繼續前往「Platform Server管理設定」頁面。 視需要輸入新值或接受預設值。

   您可以設定下列項目：

<table id="table_AA5D7674BBBE4AD4B373066AEF413FFD"> 
 <tbody> 
  <tr> 
   <td> <p> 平台伺服器HTTP連接埠 </p> </td> 
   <td> <p>影像提供與影像轉譯的主要HTTP監聽埠 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 管理員監聽埠 </p> </td> 
   <td> <p>管理員監聽埠 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 平台伺服器快取大小(MB) </p> </td> 
   <td> <p>主響應快取的初始大小 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 平台伺服器快取位置 </p> </td> 
   <td> <p>PS快取資料夾 </p> </td> 
  </tr> 
 </tbody> 
</table>

指定的埠號必須是唯一的，並且不被其他應用程式或服務使用。

下一個螢幕提供了查看所選設定的機會。
1. 按一下&#x200B;**[!UICONTROL Back]**&#x200B;進行更改，或按一下&#x200B;**[!UICONTROL Next]**&#x200B;開始安裝。
1. 按一下&#x200B;**[!UICONTROL 完成]**&#x200B;退出安裝嚮導。
