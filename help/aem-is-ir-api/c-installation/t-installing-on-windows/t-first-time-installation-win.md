---
title: 首次安裝
description: 使用這些步驟在Windows上首次安裝映像服務。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4e34d78c-1b5b-45cf-acc5-ff12cbc6ed01
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 0%

---

# 首次安裝{#installing-for-the-first-time}

使用這些步驟在Windows上首次安裝映像服務。

1. 以管理權限登入您的伺服器主機。
1. 如果您已收到許可證，請將其複製到伺服器，然後按兩下該檔案運行許可證安裝。

   如果您尚未獲得許可證，則可以繼續安裝，並稍後安裝該許可證。

1. 解壓縮Image Serving分送Zip檔案的內容。
1. 運行以啟動安裝嚮導 [!DNL setup]/ [!DNL setup.exe].
1. 選擇 **[!UICONTROL 下一個]** 若要進入使用者授權合約(EULA)，請閱讀授權合約，然後選取 **[!UICONTROL 是]**.

   此 [!DNL Authentication] 對話框。
1. 如果已安裝許可證，且許可證資訊顯示在 [!DNL Authentication] 對話框，選擇 **[!UICONTROL 下一個]** 繼續。

   如果您沒有許可證，請選擇 **[!UICONTROL 要求授權]**. 下一個對話框顯示您電腦的其中一個網路介面卡MAC地址。 以電子郵件傳送此MAC地址、您的公司名稱，以及您要安裝的產品，如提示所指示。

   **重要：** 該許可證基於此主機上安裝的其中一個網路介面卡的MAC地址。 如果禁用、刪除或更換此卡，則不再將許可證識別為有效。 請務必獲得用於映像服務的硬體配置的許可證。

   您可以繼續安裝IS（沒有有效的許可證），然後安裝該許可證。 若要繼續，請選取 **[!UICONTROL 返回]** 返回 [!DNL Authentication] 對話框，然後選擇 **[!UICONTROL 下一個]**.
1. 繼續到「[!DNL Platform Server] 管理設定」頁面。 視需要輸入新值或接受預設值。

   您可以設定下列項目：

   <table id="table_AA5D7674BBBE4AD4B373066AEF413FFD"> 
   <tbody> 
   <tr> 
      <td> <p> [!DNL Platform Server] HTTP連接埠 </p> </td>
      <td> <p>影像提供與影像轉譯的主要HTTP監聽埠 </p> </td>
   </tr> 
   <tr> 
      <td> <p> 管理員監聽埠 </p> </td>
      <td> <p>管理員監聽埠 </p> </td>
   </tr> 
   <tr> 
      <td> <p> [!DNL Platform Server] 快取大小(MB) </p> </td>
      <td> <p>主響應快取的初始大小 </p> </td>
   </tr>
   <tr> 
      <td> <p> [!DNL Platform Server] 快取位置 </p> </td>
      <td> <p>PS快取資料夾 </p> </td>
   </tr>
   </tbody>
   </table>

   指定的埠號必須是唯一的，並且不被其他應用程式或服務使用。

   下一個螢幕提供了查看所選設定的機會。

1. 選擇 **[!UICONTROL 返回]** 進行更改，或選擇 **[!UICONTROL 下一個]** 以開始安裝。

1. 選擇 **[!UICONTROL 完成]** 退出安裝嚮導。
