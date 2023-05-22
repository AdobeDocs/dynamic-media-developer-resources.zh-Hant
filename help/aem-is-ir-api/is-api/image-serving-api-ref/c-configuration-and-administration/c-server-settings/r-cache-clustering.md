---
description: 將這些伺服器設定用於快取群集。
solution: Experience Manager
title: 快取群集
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: bd0267e7-ebf5-4995-b55e-89cb1a58de6d
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---

# 快取群集{#cache-clustering}

將這些伺服器設定用於快取群集。

## PS::cacheCluster.hosts — 主機 {#section-319d2ba2915e40ac8b5ea9b4fe26a88b}

IP地址清單，以分號分隔。 包括此主機應從中獲取快取資料的所有對等伺服器的IP地址。 為方便起見，可包括本地主機的IP地址；這允許群集中所有伺服器的配置設定相同。

## PS::cacheCluster.updateLocalCache — 更新本地快取 {#section-154c2c0af4544200a3499232bb130dde}

如果應將對等伺服器提供的快取條目複製到本地響應快取，則設定為「是」。

## PS::cacheCluster.queryTimeout — 查詢超時 {#section-8d2b10e15b3e44078d2d9bdb7c25bde0}

當從對等伺服器請求快取條目時，伺服器將等待，直到一個伺服器響應它具有此特定資料項，或直到所有對等伺服器響應它們沒有該資料項，或直到用此設定指定的時間（以毫秒為單位）過期。

## PS::cacheCluster.fetchTimeout — 提取超時 {#section-41c42a29a26f43dc9cff50ad9fae1f14}

指定伺服器等待從對等伺服器傳送實際快取資料的最大毫秒數。 如果在超時到期前未傳遞完整資料，則伺服器會假定對等方已不可用。 然後在本地生成快取條目。
