---
description: 使用這些伺服器設定進行快取叢集。
solution: Experience Manager
title: 快取叢集
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: bd0267e7-ebf5-4995-b55e-89cb1a58de6d
TQID: 'https://experienceleague.adobe.com/4SJmK1ILgnCBqYjjQcEnz0SVRzQfsY9mD05Xpd1ssnw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 200
ht-degree: 0%

---

# 快取叢集{#cache-clustering}

使用這些伺服器設定進行快取叢集。

## PS：：cacheCluster.hosts — 主機 {#section-319d2ba2915e40ac8b5ea9b4fe26a88b}

IP位址清單，以分號分隔。 包括此主機應該取得快取資料的所有對等伺服器的IP位址。 為方便起見，可能會包含本機主機的IP位址；如此可讓叢集中所有伺服器的組態設定相同。

## PS：：cacheCluster.updateLocalCache — 更新本機快取 {#section-154c2c0af4544200a3499232bb130dde}

若對等伺服器提供的快取專案應複製到本機回應快取，則設為&#39;Yes&#39;。

## ps：：cacheCluster.queryTimeout — 查詢逾時 {#section-8d2b10e15b3e44078d2d9bdb7c25bde0}

從對等伺服器要求快取專案時，伺服器會等待一個伺服器回應它有此特定資料專案，或等待所有對等伺服器回應它們沒有資料專案，或等待使用此設定指定的時間（以毫秒為單位）過期。

## PS：：cacheCluster.fetchTimeout — 擷取逾時 {#section-41c42a29a26f43dc9cff50ad9fae1f14}

指定伺服器等待從對等伺服器傳送實際快取資料的最大毫秒數。 如果逾時到期前尚未傳送完整資料，則伺服器會假設對等節點已無法使用。 然後快取專案會在本機產生。
