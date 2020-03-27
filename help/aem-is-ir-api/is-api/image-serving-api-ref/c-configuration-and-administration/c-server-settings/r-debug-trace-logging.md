---
description: 使用這些伺服器設定對跟蹤記錄進行調試。
seo-description: 使用這些伺服器設定對跟蹤記錄進行調試。
seo-title: Debug_trace記錄
solution: Experience Manager
title: Debug_trace記錄
topic: Scene7 Image Serving - Image Rendering API
uuid: 33f1d093-007d-453b-965a-9d701a845954
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Debug_trace記錄{#debug-trace-logging}

使用這些伺服器設定對跟蹤記錄進行調試。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>建議將所有日誌檔案配置為寫入到與相同的資料夾 `TC::directory`。 這可確保所有映像服務日誌檔案都參與配置為的自動日誌檔案旋轉 `TC::maxDays`，從而防止由於磁碟空間不足而導致的伺服器可能不穩定。

## SV::log —— 伺服器主管跟蹤日誌檔案路徑 {#section-3697bc480ff646e79cacc2812c55ef26}

伺服器主管日誌檔案的資料夾和基本檔案名。 路徑可以是絕對或相對 *[!DNL install_folder]*。 伺服器主管將在檔案名(如果有的話，在檔案尾碼之 *[!DNL -yyyy-mm-dd]*&#x200B;前)附加一個連字型大小和當前日期()。 建議將所有日誌檔案發送到與平台伺服器日誌檔案( `PS::LogFolder`)相同的資料夾，以利用平台伺服器( `PS::LogDays`)實施的日誌檔案管理。 預設為 [!DNL logs/Supervisor.log].

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>必須先建立新資料夾，才能變更此設定。 請確定已設定訪問權限，以便伺服器主管具有必要的建立、讀取和寫入權限。

## SV::tracelevel —— 伺服器主管跟蹤日誌級別 {#section-36f8634741da4c618d67aa628b5fe474}

日誌級別可以是1、2、3或4。 預設為 2。

## IS:：日誌——映像伺服器調試日誌檔案路徑 {#section-73a3f09b77f2446c9f82207b7d8aec39}

Image Server跟蹤日誌檔案的資料夾和基本檔案名。 路徑可以是絕對或相對 *[!DNL install_folder]*。 ImageServer會在檔案名稱(若有的話，在檔 *[!DNL -yyyy-mm-dd]*&#x200B;案尾碼之前)附加連字型大小和目前日期()。 建議將映像伺服器日誌檔案與平台伺服器日誌檔案( `PS::LogFolder`)發送到相同的資料夾，以利用平台伺服器實施的日誌檔案管理(請參見 `PS::LogDays`)。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>必須先建立新資料夾，才能變更此設定。 請確定已設定存取權限，讓「影像伺服」具有必要的建立、讀取和寫入權限。

## IS:TraceClient —— 映像伺服器調試日誌級別 {#section-3851f1f68e404430985c629ac80534db}

記錄層級可以是1、2、3或4（預設為2）

1級記錄與啟動、關閉和平台伺服器連接相關的事件。

第2級還記錄了與源映像的連接和斷開連接。

第3級增加了像素資料要求記錄，並將其傳送至平台伺服器。

4級記錄從平台伺服器收到的所有消息。

級別3和級別4應僅用於調試，因為日誌檔案可能變得非常大。

## IS::TraceStatsInterval —— 影像伺服器統計日誌間隔 {#section-1d8df96d61044e33a5b2b2b0309c2d59}

映像伺服器按此設定指定的間隔將記憶體統計資訊寫入其跟蹤日誌檔案。 有效範圍為5到86,400秒。
