---
description: 快取叢集可讓多個負載平衡的伺服器交換主要回應快取和次要資料快取中的快取專案（適用於巢狀/內嵌請求），而不需要在多部伺服器上產生相同的快取專案，因此可大幅提升伺服器回應速度。
solution: Experience Manager
title: 快取叢集
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d1bea565-ac4e-4717-a53f-cbe706664598
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 0%

---

# 快取叢集{#cache-clustering}

快取叢集可讓多個負載平衡的伺服器交換主要回應快取和次要資料快取中的快取專案（適用於巢狀/內嵌請求），而不需要在多部伺服器上產生相同的快取專案，因此可大幅提升伺服器回應速度。

如果已如此設定，當伺服器收到不在本機快取中的專案要求時，就會連絡叢集中的對等伺服器。 它會先檢查他們是否已擁有該資料專案，然後再要求影像伺服器產生專案。

快取叢集主要有利於涉及高度可快取內容的應用程式。 在初始部署期間以及使用新內容上線時，伺服器載入量應該會大幅減少。

逾時和其他防護措施可確保系統繼續以完整容量執行，即使有一或多部對等伺服器離線。

快取叢集可以下列兩種基本設定之一運作：

* 時間 `PS::cacheCluster.updateLocalCache` 已啟用（預設），對等伺服器上找到的任何快取專案都會複製到本機快取。

   此設定可減少對等伺服器之間的流量。 它也能提供最快的回應時間，但代價是將所有快取專案復寫至叢集中的所有伺服器。 這是建議的設定。

* 時間 `PS::cacheCluster.updateLocalCache` 停用，來自其他伺服器的資料不會複製到本機快取。

   這會乘以快取資料的可用磁碟空間。 但是，它會增加對等伺服器之間的流量，並減少整體回應時間。 只有在您看到低快取命中率時，才使用此設定。
