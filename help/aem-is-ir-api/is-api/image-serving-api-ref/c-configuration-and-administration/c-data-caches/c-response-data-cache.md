---
description: 平台伺服器會將所有回覆影像和特定文字資料快取至磁碟，除非請求標示為不可快取。
solution: Experience Manager
title: 回應資料快取
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---


# 響應資料快取{#response-data-cache}

平台伺服器會將所有回覆影像和特定文字資料快取至磁碟，除非請求標示為不可快取。

平台伺服器的磁碟快取的位置設定為`PS::cache.rootPaths`。

對於具有高快取命中率的應用程式，您可以通過在多個磁碟設備之間分發響應資料快取來提高伺服器效能和容量。 通過在每個磁碟上建立快取根資料夾並在`PS::cache.rootPaths`中註冊，可以完成此操作。

`PS::cache.maxSize` 指定所有快取條目的總大小，而不考慮任何檔案系統開銷。實際需要的磁碟空間量取決於檔案系統屬性（如磁碟塊大小）和快取條目數。 建議為HTTP磁碟快取保留的磁碟空間是`PS::cache.maxSize`所指定的磁碟空間的兩倍。 使用最近最少使用的演算法，將快取的資料量保持在限制內。

除了`PS::cache.maxSize`外，還通過限制具有`PS::cache.maxEntries`的最大快取條目數來管理響應快取。 在Linux上，此設定必須指定一個不大於快取分區上可用indo的數目的值。

>[!NOTE]
>
>平台伺服器維護記憶體中快取索引。 此索引的大小是`PS::cache.maxEntries`值的32個位元組。 您可能需要增加平台伺服器堆大小以容納較大的快取。

當伺服器按順序關閉時，系統使用快取索引檔案保存到磁碟。 如果發生意外事件（如電源故障），則可能無法保存此檔案。 此外，平台伺服器可能需要幾分鐘的時間才能準備就緒。
