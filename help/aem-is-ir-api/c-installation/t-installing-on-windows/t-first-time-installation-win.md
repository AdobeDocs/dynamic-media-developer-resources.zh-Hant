---
title: 首次安裝
description: 使用這些步驟在Windows上首次安裝Image Service。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4e34d78c-1b5b-45cf-acc5-ff12cbc6ed01
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 0%

---

# 首次安裝{#installing-for-the-first-time}

使用這些步驟在Windows上首次安裝Image Service。

1. 使用管理權限登錄到伺服器主機。
1. 如果您已收到許可證，請將其複製到伺服器，然後按兩下該檔案運行許可證安裝。

   如果您尚未獲得許可證，則可以稍後繼續安裝並安裝許可證。

1. 提取Image Service分發zip檔案的內容。
1. 運行以啟動安裝嚮導 [!DNL setup]/ [!DNL setup.exe]。
1. 選擇 **[!UICONTROL 下一個]** 要進入最終用戶許可協定(EULA)，請閱讀許可協定，然後選擇 **[!UICONTROL 是]**。

   的 [!DNL Authentication] 對話框。
1. 如果已安裝許可證，且許可證資訊顯示在 [!DNL Authentication] 對話框，選擇 **[!UICONTROL 下一個]** 繼續。

   如果您沒有許可證，請選擇 **[!UICONTROL 請求許可證]**。 下一個對話框顯示電腦的網路介面卡MAC地址之一。 按照提示的指示，向此MAC地址、您的公司名稱和您正在安裝的產品發送電子郵件。

   **重要提示：** 許可證基於此主機上安裝的一個網路介面卡的MAC地址。 如果禁用、刪除或更換此卡，則許可證不再被識別為有效。 確保獲取用於映像服務的硬體配置的許可證。

   您可以繼續安裝沒有有效許可證的IS，稍後再安裝該許可證。 要繼續，請選擇 **[!UICONTROL 後退]** 返回 [!DNL Authentication] 對話框，然後選擇 **[!UICONTROL 下一個]**。
1. 繼續到「平台伺服器管理設定」頁。 根據需要輸入新值或接受預設值。

   可以配置以下項目：

   <table id="table_AA5D7674BBBE4AD4B373066AEF413FFD"> 
   <tbody> 
   <tr> 
      <td> <p> 平台伺服器HTTP連接埠 </p> </td>
      <td> <p>用於影像服務和影像呈現的主HTTP偵聽埠 </p> </td>
   </tr> 
   <tr> 
      <td> <p> 管理員偵聽埠 </p> </td>
      <td> <p>管理員偵聽埠 </p> </td>
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

   指定的埠號必須唯一且不被其他應用程式或服務使用。

   下一螢幕提供了查看所選設定的機會。

1. 選擇 **[!UICONTROL 後退]** 進行更改，或 **[!UICONTROL 下一個]** 來啟動安裝。

1. 選擇 **[!UICONTROL 完成]** ，可退出安裝嚮導。
