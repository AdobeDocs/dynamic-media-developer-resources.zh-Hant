---
description: 使用這些伺服器設定調試跟蹤記錄。
solution: Experience Manager
title: Debug_trace記錄
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: fe1fc984-3c6b-4bd1-b5ba-630860ac7319
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---

# Debug_trace記錄{#debug-trace-logging}

使用這些伺服器設定調試跟蹤記錄。

>[!NOTE]
>
>建議將所有要寫入與`TC::directory`相同的資料夾的日誌檔案配置為。 這可確保所有映像服務日誌檔案都參與配置為`TC::maxDays`的自動日誌檔案旋轉，這將防止由於磁碟空間不足情況而可能出現的伺服器不穩定。

## SV::log — 伺服器主管跟蹤日誌檔案路徑 {#section-3697bc480ff646e79cacc2812c55ef26}

伺服器主管日誌檔案的資料夾和基本檔案名。 路徑可以是絕對路徑，也可以是相對於&#x200B;*[!DNL install_folder]*&#x200B;的路徑。 伺服器主管將在檔案名中附加連字型大小和當前日期(*[!DNL -yyyy-mm-dd]*)（在檔案尾碼前，如果有）。 建議將所有日誌檔案發送到與Platform Server日誌檔案(`PS::LogFolder`)相同的資料夾，以利用由Platform Server(`PS::LogDays`)實施的日誌檔案管理。 預設為 [!DNL logs/Supervisor.log].

>[!NOTE]
>
>更改此設定之前必須建立新資料夾。 確保已設定訪問權限，使伺服器主管具有必要的建立、讀取和寫入權限。

## SV::tracelevel — 伺服器主管跟蹤日誌級別 {#section-36f8634741da4c618d67aa628b5fe474}

記錄層級可以是1、2、3或4。 預設為 2。

## IS::Log — 映像伺服器調試日誌檔案路徑 {#section-73a3f09b77f2446c9f82207b7d8aec39}

映像伺服器跟蹤日誌檔案的資料夾和基本檔案名。 路徑可以是絕對路徑，也可以是相對於&#x200B;*[!DNL install_folder]*&#x200B;的路徑。 ImageServer將在檔案名中附加連字型大小和當前日期(*[!DNL -yyyy-mm-dd]*)（在檔案尾碼前，如果有）。 建議將映像伺服器日誌檔案發送到與平台伺服器日誌檔案相同的資料夾(`PS::LogFolder`)，以利用平台伺服器實施的日誌檔案管理（請參見`PS::LogDays`）。

>[!NOTE]
>
>更改此設定之前必須建立新資料夾。 請確定已設定存取權限，讓影像伺服器具有必要的建立、讀取和寫入權限。

## IS:TraceClient — 映像伺服器調試日誌級別 {#section-3851f1f68e404430985c629ac80534db}

記錄層級可以是1、2、3或4（預設為2）

第1級記錄與啟動、關閉和Platform Server連接相關的事件。

第2級還記錄連接和斷開源映像的連接。

第3層新增了像素資料請求記錄，並將其傳送至Platform伺服器。

4級記錄從Platform Server接收的所有消息。

級別3和級別4隻應用於調試，因為日誌檔案可能會變得非常大。

## IS::TraceStatsInterval — 影像伺服器統計日誌間隔 {#section-1d8df96d61044e33a5b2b2b0309c2d59}

映像伺服器按此設定指定的間隔將記憶體統計資訊寫入其跟蹤日誌檔案。 有效範圍是5到86,400秒。
