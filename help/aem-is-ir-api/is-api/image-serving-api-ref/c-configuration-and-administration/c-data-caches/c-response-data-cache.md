---
description: 此 [!DNL Platform Server] 快取所有回復影像和某些文本資料到磁碟，除非將請求標籤為不可快取。
solution: Experience Manager
title: 回應資料快取
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: f09e596d-2b85-4950-8515-d54a2c2e86ae
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# 回應資料快取{#response-data-cache}

此 [!DNL Platform Server] 快取所有回復影像和某些文本資料到磁碟，除非將請求標籤為不可快取。

的位置 [!DNL Platform Server]&#39;s磁碟快取已設定為 `PS::cache.rootPaths`.

對於快取命中率高的應用程式，您可以在多個磁碟設備之間分配響應資料快取，從而提高伺服器效能和容量。 要完成此操作，請在每個磁碟上建立快取根資料夾，並在中註冊 `PS::cache.rootPaths`.

`PS::cache.maxSize` 指定所有快取項的總大小，而不考慮任何檔案系統開銷。 實際需要的磁碟空間量取決於檔案系統屬性（如磁碟塊大小）和快取條目數。 建議為HTTP磁碟快取保留兩倍於 `PS::cache.maxSize`. 使用最近使用的算法將快取資料量保持在限制內。

除 `PS::cache.maxSize`，響應快取也通過限制快取條目的最大數量來管理 `PS::cache.maxEntries`. 在Linux上，此設定必須指定的值不得大於快取分區上的可用inode數。

>[!NOTE]
>
>此 [!DNL Platform Server] 維護記憶體內快取索引。 此索引的大小是 `PS::cache.maxEntries`. 您可能需要增加 [!DNL Platform Server] 堆大小以容納較大的快取。

系統使用快取索引檔案，當伺服器按順序關閉時，該檔案會保存到磁碟。 如果發生非預期事件（如電源故障），則可能無法保存此檔案。 此外，可能需要幾分鐘的時間才能 [!DNL Platform Server] 準備好了。
