---
title: 回應資料快取
description: 此 [!DNL Platform Server] 除非要求標示為無法快取，否則會將所有回覆影像和特定文字資料快取到磁碟。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: f09e596d-2b85-4950-8515-d54a2c2e86ae
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# 回應資料快取{#response-data-cache}

此 [!DNL Platform Server] 除非要求標示為不可快取，否則會將所有回覆影像和特定文字資料快取到磁碟。

的位置 [!DNL Platform Server]的磁碟快取設定為 `PS::cache.rootPaths`.

對於快取命中率高的應用程式，您可以在多個磁碟裝置之間分配回應資料快取，以提高伺服器效能和容量。 您可以在每個磁碟上建立快取根資料夾，並在中註冊這些資料夾，以達成此目的 `PS::cache.rootPaths`.

此 `PS::cache.maxSize` 指定所有快取專案的總大小，不考慮任何檔案系統負荷。 所需的磁碟空間量取決於檔案系統屬性（例如磁碟區塊大小）和快取專案數。 為HTTP磁碟快取保留的磁碟空間是指定的數量的兩倍 `PS::cache.maxSize`. 採用最近最少使用的演演算法，將快取資料量保持在限制內。

除了 `PS::cache.maxSize`，回應快取也可透過以下限制來管理 `PS::cache.maxEntries`. 在Linux®上，此設定所指定的值不得大於快取分割區上可用的inode數目。

>[!NOTE]
>
>此 [!DNL Platform Server] 維護記憶體中的快取索引。 此索引的大小是32位元組乘以值 `PS::cache.maxEntries`. 增加 [!DNL Platform Server] 若有需要，棧積大小可容納較大的快取。

當伺服器依序關閉時，系統會使用儲存至磁碟的快取索引檔案。 如果發生意外事件（例如電源故障），可能無法儲存此檔案。 此外，可能需要幾分鐘的時間才能完成 [!DNL Platform Server] 準備就緒。
