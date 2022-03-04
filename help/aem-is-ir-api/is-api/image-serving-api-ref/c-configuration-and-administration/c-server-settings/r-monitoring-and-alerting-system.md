---
description: 使用這些伺服器設定配置監視和警報系統。
solution: Experience Manager
title: 監視和警報系統
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: fe672d1b-93e5-466a-a329-3032095c6ba8
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---

# 監視和警報系統{#monitoring-and-alerting-system}

使用這些伺服器設定配置監視和警報系統。

## AS::monitorAlertGenerator.enableGlobalAlerting — 警報系統啟用 {#section-612f8ea61794426ab205e22e5f665fa9}

通過設定為「true」並配置電子郵件通知設定來啟用電子郵件通知。 設定為 `false` 關閉所有電子郵件警報 — 當使伺服器離線以進行維護時，此功能非常有用。 布林.

## AS::mailSender.host - SMTP主機 {#section-151df07e7b44446581339bb7abeeba7a}

SMTP電子郵件伺服器的IP地址。

## AS::mailSender.port- SMTP埠 {#section-4b25efca8fd84d5c92dafacd0555e99d}

SMTP電子郵件伺服器的偵聽埠。

## AS::monitorAlertGenerator.messageTo — 郵件收件人 {#section-0017bbaa15434117a70900c3f1163960}

應向其發送警報的一個或多個電子郵件地址。 使用分號作為分隔符。

## AS::monitorAlertGenerator.messageFrom — 消息發件人 {#section-db320cba4ac2438ca1cfe6abce4aed87}

在中應使用的電子郵件地址 **[!UICONTROL 從]** 電子郵件欄位。

## AS::monitorAlertGenerator.alertInterval — 監視間隔 {#section-99cb2e3380c1499e9d5aec3671ed73c7}

監視系統將在警報間隔期間累積警報條件，並在每個間隔結束時發送包含所有累積警報的警報電子郵件。 毫秒、整數值、60000或更大。 通常設定為5或10分鐘。

## AS::monitorAlertGenerator.heapSpaceResetInterval — 堆空間警報間隔 {#section-fd5a2bf04ed44fdcaef20f77084151a8}

在發出堆空間警報之後的最短時間。 間隔時間（毫秒）。 整數值，0或更大。

## AS::monitorAlertGenerator.minTrafficForAlerts — 要啟用警報的最小通信量 {#section-8b4db2d6f96642309ca35c49eb3ab230}

每秒請求數。 如果通信量低於此閾值，則不會發出響應時間和錯誤警報。 設定為0以發送響應時間和錯誤警報，而不考慮通信量。 實際值0或更大。
