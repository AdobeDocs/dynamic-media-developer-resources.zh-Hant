---
description: 快取群集允許多個負載平衡伺服器在主響應快取和輔助資料快取中交換快取條目（對於嵌套／嵌入請求），通過消除在多個伺服器上生成相同快取條目的需要，有可能顯著提高伺服器響應性。
solution: Experience Manager
title: 快取叢集
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---


# 快取群集{#cache-clustering}

快取群集允許多個負載平衡伺服器在主響應快取和輔助資料快取中交換快取條目（對於嵌套／嵌入請求），通過消除在多個伺服器上生成相同快取條目的需要，有可能顯著提高伺服器響應性。

如果已配置，則當伺服器收到對不在本地快取中的項的請求時，它將與群集中的對等伺服器聯繫。 它會先檢查他們是否已擁有該資料項目，再要求影像伺服器產生該項目。

快取群集主要有利於涉及高可快取內容的應用程式。 在初次部署期間和新內容上線時，伺服器負載應大幅降低。

超時和其他保護功能可確保即使一個或多個對等伺服器處於離線狀態，系統仍能繼續以滿容量運行。

快取群集可以在以下兩種基本配置之一中運行：

* 啟用`PS::cacheCluster.updateLocalCache`時（預設），在對等伺服器上找到的任何快取條目都會複製到本地快取。

   此配置會減少對等伺服器之間的通信量。 它還提供最快的響應時間，而代價是將所有快取條目複製到群集中的所有伺服器。 這是建議的設定。

* 當`PS::cacheCluster.updateLocalCache`被禁用時，來自未複製到本地快取中的其他伺服器的資料。

   這將快取資料的可用磁碟空間相乘。 但是，它會增加對等伺服器之間的流量，並減少整體回應時間。 只有在您看到低快取點擊率時，才使用此設定。

