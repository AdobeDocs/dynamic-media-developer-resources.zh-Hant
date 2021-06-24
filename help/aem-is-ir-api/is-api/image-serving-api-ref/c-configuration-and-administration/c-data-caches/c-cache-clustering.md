---
description: 快取群集允許多個負載平衡伺服器在主響應快取和輔助資料快取中交換快取條目（針對嵌套/嵌入請求），通過消除在多個伺服器上生成相同快取條目的需要，可能顯著提高伺服器響應。
solution: Experience Manager
title: 快取群集
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: d1bea565-ac4e-4717-a53f-cbe706664598
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 0%

---

# 快取群集{#cache-clustering}

快取群集允許多個負載平衡伺服器在主響應快取和輔助資料快取中交換快取條目（針對嵌套/嵌入請求），通過消除在多個伺服器上生成相同快取條目的需要，可能顯著提高伺服器響應。

如果配置了，則當伺服器收到對不在本地快取中的項的請求時，它將與群集中的對等伺服器聯繫。 它會在要求影像伺服器產生項目之前，檢查他們是否已擁有該資料項目。

快取群集主要有利於涉及高度可快取內容的應用程式。 在初始部署期間和隨新內容上線時，伺服器負載應大幅減少。

超時和其他保護措施可確保即使一個或多個對等伺服器離線，系統仍能以完全容量繼續運行。

快取群集可在以下兩種基本配置之一中運作：

* 當`PS::cacheCluster.updateLocalCache`啟用時（預設值），在對等伺服器上找到的任何快取條目都將複製到本地快取。

   此配置減少了對等伺服器之間的通信量。 它還提供最快的響應時間，而代價是將所有快取項複製到群集中的所有伺服器。 這是建議的設定。

* 當`PS::cacheCluster.updateLocalCache`被禁用時，來自其他伺服器的資料不會複製到本地快取。

   這將快取資料的可用磁碟空間乘以。 但是，它會增加對等伺服器之間的流量並減少整體回應時間。 只有在出現低快取點擊率時，才使用此設定。
