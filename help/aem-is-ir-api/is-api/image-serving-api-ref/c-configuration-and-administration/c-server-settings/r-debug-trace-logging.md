---
description: 使用這些伺服器設定調試跟蹤記錄。
solution: Experience Manager
title: Debug_trace日誌記錄
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: fe1fc984-3c6b-4bd1-b5ba-630860ac7319
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 1%

---

# Debug_trace日誌記錄{#debug-trace-logging}

使用這些伺服器設定調試跟蹤記錄。

>[!NOTE]
>
>建議將所有日誌檔案配置為與 `TC::directory`。 這可確保所有Image Serving日誌檔案都參與配置為自動日誌檔案旋轉 `TC::maxDays`這將防止由於磁碟空間不足而導致的伺服器不穩定。

## SV::log — 伺服器主管跟蹤日誌檔案路徑 {#section-3697bc480ff646e79cacc2812c55ef26}

伺服器主管日誌檔案的資料夾和基本檔案名。 路徑可以是絕對的，也可以是相對於 *[!DNL install_folder]*。 伺服器主管將追加連字元和當前日期( *[!DNL -yyyy-mm-dd]*)到檔案名（在檔案尾碼之前，如果有）。 建議將所有日誌檔案發送到與 [!DNL Platform Server] 日誌檔案( `PS::LogFolder`)，以利用 [!DNL Platform Server] ( `PS::LogDays`)。 預設為 [!DNL logs/Supervisor.log].

>[!NOTE]
>
>必須先建立新資料夾，然後才能更改此設定。 確保設定了訪問權限，以便伺服器主管具有必要的建立、讀取和寫入權限。

## SV::tracelevel — 伺服器主管跟蹤日誌級別 {#section-36f8634741da4c618d67aa628b5fe474}

日誌級別可以是1、2、3或4。 預設為 2。

## IS:：日誌 — 映像伺服器調試日誌檔案路徑 {#section-73a3f09b77f2446c9f82207b7d8aec39}

Image Server跟蹤日誌檔案的資料夾和基本檔案名。 路徑可以是絕對的，也可以是相對於 *[!DNL install_folder]*。 ImageServer將添加連字元和當前日期( *[!DNL -yyyy-mm-dd]*)到檔案名（在檔案尾碼之前，如果有）。 建議將映像伺服器日誌檔案發送到與 [!DNL Platform Server] 日誌檔案( `PS::LogFolder`)，以利用 [!DNL Platform Server] （請參見） `PS::LogDays`)。

>[!NOTE]
>
>必須先建立新資料夾，然後才能更改此設定。 確保設定了訪問權限，以便映像服務具有必要的建立、讀取和寫入權限。

## IS:TraceClient — 映像伺服器調試日誌級別 {#section-3851f1f68e404430985c629ac80534db}

日誌級別可以是1、2、3或4（預設值為2）

1級記錄與啟動、關閉和 [!DNL Platform Server] 連接。

級別2還記錄與源映像的連接和斷開。

第3級添加對像素資料的請求的記錄，並將其發送到 [!DNL Platform Server]。

4級記錄從 [!DNL Platform Server]。

級別3和級別4應僅用於調試目的，因為日誌檔案可能會變得非常大。

## IS::TraceStatsInterval — 映像伺服器統計日誌間隔 {#section-1d8df96d61044e33a5b2b2b0309c2d59}

映像伺服器按此設定指定的間隔將記憶體統計資訊寫入其跟蹤日誌檔案。 有效範圍為5到86,400秒。
