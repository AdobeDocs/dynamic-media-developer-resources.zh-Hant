---
description: 使用這些伺服器設定進行快取叢集。
solution: Experience Manager
title: 快取叢集
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---


# 快取群集{#cache-clustering}

使用這些伺服器設定進行快取叢集。

## PS::cacheCluster.hosts —— 主機{#section-319d2ba2915e40ac8b5ea9b4fe26a88b}

IP位址清單，以分號分隔。 包含此主機應從中獲取快取資料的所有對等伺服器的IP地址。 本地主機的IP地址可以包含，方便使用；這允許群集中所有伺服器的配置設定相同。

## PS::cacheCluster.updateLocalCache —— 更新本地快取{#section-154c2c0af4544200a3499232bb130dde}

如果應將對等伺服器提供的快取條目複製到本地響應快取，則設定為「是」。

## PS::cacheCluster.queryTimeout —— 查詢超時{#section-8d2b10e15b3e44078d2d9bdb7c25bde0}

從對等伺服器請求快取項目時，伺服器會等到一個伺服器回應其含有此特定資料項目，或直到所有對等伺服器回應其沒有該資料項目，或直到使用此設定指定的時間（以毫秒為單位）過期。

## PS::cacheCluster.fetchTimeout - Fetch Timeout {#section-41c42a29a26f43dc9cff50ad9fae1f14}

指定伺服器等待從對等伺服器傳送的實際快取資料的最大毫秒數。 如果在逾時到期前未傳送完整資料，伺服器會假設對等項目已變為無法使用。 然後在本地生成快取條目。
