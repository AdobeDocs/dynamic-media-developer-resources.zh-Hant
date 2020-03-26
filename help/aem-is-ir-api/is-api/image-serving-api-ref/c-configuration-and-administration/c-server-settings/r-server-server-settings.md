---
description: 使用這些伺服器設定來配置伺服器。
seo-description: 使用這些伺服器設定來配置伺服器。
seo-title: 伺服器
solution: Experience Manager
title: 伺服器
topic: Scene7 Image Serving - Image Rendering API
uuid: 50db98cc-8354-4884-9416-00808828061b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 伺服器{#server}

使用這些伺服器設定來配置伺服器。

## SV::ImageServerMode —— 影像伺服器模式 {#section-991b287f2dde4f77a24fc69d5b32cabd}

32位和64位版本的映像伺服器都可用於Linux。 當安裝在64位元Linux伺服器上時，請指定ImageServer64；當安裝在32位元伺服器上時，請指定ImageServer32（預設）。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>64位元版本的Image Server不支援FlashPix來源檔案。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>Windows不支援64位元模式。 只能 `ImageServer32` 指定。 否則，將不會啟動「影像伺服」。

## SV::PsHeapSize —— 平台伺服器堆積大小 {#section-fd83715948764aeda58d6b3a9f9f8be9}

平台伺服器的Java堆大小。 預設為「 `512m`」(512 MB)。

## IS::TcpPort,PS::isConnection.port —— 映像伺服器偵聽埠 {#section-5421bfd2ca2a4a979faf812b6fdb2887}

指定用於平台伺服器和映像伺服器之間通信的埠。 請務必指定主機系統上未使用的埠號。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>若要讓「影像伺服」正常運作，必須為和設定相 `IS::TcpPort` 同值 `PS::isConnection.port`。

## IS:：物理記憶體——映像伺服器記憶體限制 {#section-85e37aa2ac6e456eb698da716dd3247d}

記憶體中影像資料的近似限制，以物理記憶體的百分比表示。 有效範圍為10%到90%。 如果可能，映像伺服器會嘗試將其對映像記憶體的使用限制在指定數量。 在繁重的處理活動期間，可以暫時超過限制。

## IS::WorkerThreads —— 映像伺服器工作線程數 {#section-e2946063b13c4f728cdf5dba3d8b4de1}

影像伺服器用於處理影像資料的最大執行緒數。 預設值為0，這允許影像伺服器自動優化線程數。

某些作業系統具有線程模型，上下文切換開銷高。 在這種情況下，當選擇特定線程計數時（例如每CPU一個線程），整體伺服器效能可以提高。 為了尋找最佳的設定，可能需要進行一些實驗。 如需詳細資訊，請參閱影像伺服發行說明和作業系統檔案。

## IS::NumberOfTextServers —— 文字伺服器例項數 {#section-971e20a90c1a473598fba738ed95671a}

同時作用的文字轉譯器數目上限。 0（預設值）等於1.5倍可用CPU核心數。

## IS::TextServerTcpPortRange —— 文本伺服器通信埠 {#section-a13465de88ed4df09931e5ba840c1942}

用於文本伺服器通信的埠。 指定第一個和最後一個埠號，以&#39;-&#39;分隔。
