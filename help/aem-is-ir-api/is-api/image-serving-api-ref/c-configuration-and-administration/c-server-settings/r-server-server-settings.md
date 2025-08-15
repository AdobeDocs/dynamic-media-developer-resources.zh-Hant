---
description: 使用這些伺服器設定來設定您的伺服器。
solution: Experience Manager
title: 伺服器
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 10970ca8-b209-4adf-b027-6eb8d7a15db6
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 0%

---

# 伺服器{#server}

使用這些伺服器設定來設定您的伺服器。

## SV：：ImageServerMode — 影像伺服器模式 {#section-991b287f2dde4f77a24fc69d5b32cabd}

Image Server的32位元和64位元版本皆適用於Linux。 若安裝在64位元Linux伺服器上，請指定ImageServer64；若安裝在32位元伺服器上，請指定ImageServer32 （預設）。

>[!NOTE]
>
>Image Server的64位元版本不支援FlashPix來源檔案。

>[!NOTE]
>
>Windows不支援64位元模式。 只能指定`ImageServer32`。 否則，影像伺服不會啟動。

## SV：：PsHeapSize - [!DNL Platform Server]棧積大小 {#section-fd83715948764aeda58d6b3a9f9f8be9}

[!DNL Platform Server]的Java棧積大小。 預設為&quot; `512m`&quot; (512 MB)。

## IS：：TcpPort， PS：：isConnection.port — 影像伺服器接聽連線埠 {#section-5421bfd2ca2a4a979faf812b6fdb2887}

指定用於[!DNL Platform Server]和影像伺服器之間通訊的連線埠。 請務必指定在主機系統上不會使用的連線埠號碼。

>[!NOTE]
>
>若要讓「影像伺服」正常運作，必須為`IS::TcpPort`和`PS::isConnection.port`設定相同的值。

## IS：：PhysicalMemory — 影像伺服器記憶體限制 {#section-85e37aa2ac6e456eb698da716dd3247d}

記憶體內部影像資料的大約限制，以實體記憶體的百分比表示。 有效範圍為10%到90%。 如果可能，影像伺服器會嘗試將影像記憶體的使用限製為指定的數量。 在繁重處理作業期間，可能會暫時超過限制。

## IS：：WorkerThreads — 影像伺服器背景工作Threads的數量 {#section-e2946063b13c4f728cdf5dba3d8b4de1}

影像伺服器用於處理影像資料的最大執行緒數量。 預設值為0，可讓影像伺服器自動最佳化執行緒計數。

有些作業系統的執行緒模型具有高的內容切換負荷。 在這種情況下，選取特定執行緒計數時(例如，每個CPU一個執行緒)，整體伺服器效能可能會改善。 可能需要一些實驗來尋找最佳設定。 如需詳細資訊，請參閱「影像伺服」發行說明和作業系統檔案。

## IS：：NumberOfTextServers — 文字伺服器執行處理數目 {#section-971e20a90c1a473598fba738ed95671a}

同時作用中的最大文字轉譯器數目。 0 （預設）等於可用CPU核心數量的1.5倍。

## IS：：TextServerTcpPortRange — 文字伺服器通訊連線埠 {#section-a13465de88ed4df09931e5ba840c1942}

用於文字伺服器通訊的連線埠。 指定第一個和最後一個連線埠號碼，以&#39;-&#39;分隔。
