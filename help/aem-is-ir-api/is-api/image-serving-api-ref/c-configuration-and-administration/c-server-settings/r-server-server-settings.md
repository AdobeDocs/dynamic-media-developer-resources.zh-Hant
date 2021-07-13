---
description: 使用這些伺服器設定配置您的伺服器。
solution: Experience Manager
title: 伺服器
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: 10970ca8-b209-4adf-b027-6eb8d7a15db6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 0%

---

# 伺服器{#server}

使用這些伺服器設定配置您的伺服器。

## SV::ImageServerMode — 影像伺服器模式 {#section-991b287f2dde4f77a24fc69d5b32cabd}

32位和64位版本的映像伺服器均適用於Linux。 當安裝在64位Linux伺服器上時，請指定ImageServer64，當安裝在32位伺服器上時，指定ImageServer32（預設值）。

>[!NOTE]
>
>64位版本的Image Server不支援FlashPix源檔案。

>[!NOTE]
>
>Windows不支援64位模式。 只能指定`ImageServer32`。 否則，將不會啟動「影像伺服」。

## SV::PsHeapSize — 平台伺服器堆大小 {#section-fd83715948764aeda58d6b3a9f9f8be9}

平台伺服器的Java堆大小。 預設為&quot; `512m`&quot;(512 MB)。

## IS::TcpPort, PS::isConnection.port — 映像伺服器偵聽埠 {#section-5421bfd2ca2a4a979faf812b6fdb2887}

指定用於平台伺服器和映像伺服器之間通信的埠。 請務必指定主機系統上未使用的埠號。

>[!NOTE]
>
>為了讓「影像伺服」正常運作，必須為`IS::TcpPort`和`PS::isConnection.port`設定相同的值。

## IS::PhysicalMemory — 映像伺服器記憶體限制 {#section-85e37aa2ac6e456eb698da716dd3247d}

記憶體內影像資料的近似限制，以物理記憶體的百分比表示。 有效範圍是10%到90%。 如果可能，映像伺服器會嘗試將其對映像記憶體的使用限制為指定的數量。 在繁重的處理活動期間，可能會暫時超過限制。

## IS::WorkerThreads — 映像伺服器工作線程數 {#section-e2946063b13c4f728cdf5dba3d8b4de1}

影像伺服器用於處理影像資料的最大線程數。 預設值為0，允許影像伺服器自動優化線程計數。

某些作業系統具有線程模型，上下文切換開銷高。 在這種情況下，當選擇特定線程計數時（例如每個CPU一個線程），整體伺服器效能可能得到改善。 可能需要一些實驗才能找到最佳設定。 如需詳細資訊，請參閱影像伺服發行說明和作業系統檔案。

## IS::NumberOfTextServers — 文字伺服器例項數 {#section-971e20a90c1a473598fba738ed95671a}

同時處於活動狀態的文本轉換器的最大數量。 0（預設值）等於可用CPU內核數的1.5倍。

## IS::TextServerTcpPortRange — 文本伺服器通信埠 {#section-a13465de88ed4df09931e5ba840c1942}

用於文本伺服器通信的埠。 指定第一個和最後一個埠號，用「 — 」分隔。
