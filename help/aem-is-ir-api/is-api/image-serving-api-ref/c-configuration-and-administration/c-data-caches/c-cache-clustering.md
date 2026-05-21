---
description: 快取叢集可讓多個負載平衡伺服器交換主要回應快取和次要資料快取中的快取專案（針對巢狀/內嵌請求），如此便不需在多個伺服器上產生相同的快取專案，即可大幅提升伺服器回應速度。
solution: Experience Manager
title: 快取叢集
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d1bea565-ac4e-4717-a53f-cbe706664598
TQID: 'https://experienceleague.adobe.com/J1QtNEy9i67oveb1oS2V6-fagqrrlC30oih8AS1g-N4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 305
ht-degree: 0%

---

# 快取叢集{#cache-clustering}

快取叢集可讓多個負載平衡伺服器交換主要回應快取和次要資料快取中的快取專案（針對巢狀/內嵌請求），如此便不需在多個伺服器上產生相同的快取專案，即可大幅提升伺服器回應速度。

如果已如此設定，當伺服器收到不在本機快取中的專案的要求時，它會連絡叢集中的對等伺服器。 它會先檢查他們是否已擁有該資料專案，再要求影像伺服器產生專案。

快取叢集主要有利於涉及高度可快取內容的應用程式。 在初始部署期間和使用新內容上線時，伺服器載入應大幅減少。

逾時和其他保護措施可確保系統繼續以完整容量執行，即使有一或多部對等伺服器離線。

快取叢集可以兩種基本組態之一運作：

* 啟用`PS::cacheCluster.updateLocalCache`時（預設），對等伺服器上找到的任何快取專案都會複製到本機快取。

  此設定可減少對等伺服器之間的流量。 它也能提供最快的回應時間，但成本是讓所有快取專案都複製到叢集中的所有伺服器。 這是建議的設定。

* 停用`PS::cacheCluster.updateLocalCache`時，不會將中其他伺服器的資料複製到本機快取。

  這會將快取資料的可用磁碟空間相乘。 但是，這會增加對等伺服器之間的流量，並減少整體的回應時間。 只有在您看到低快取命中率時才使用此設定。
