---
description: 使用這些伺服器設定來配置監視和警報系統。
solution: Experience Manager
title: 監視和警報系統
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: fe672d1b-93e5-466a-a329-3032095c6ba8
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---

# 監視和警報系統{#monitoring-and-alerting-system}

使用這些伺服器設定來配置監視和警報系統。

## AS::monitorAlertGenerator.enableGlobalAlerting — 警報系統啟用 {#section-612f8ea61794426ab205e22e5f665fa9}

將設為「true」並設定電子郵件通知設定，以啟用電子郵件通知。 設為`false`會關閉所有電子郵件警報 — 這在讓伺服器離線進行維護時很有用。 布林.

## AS::mailSender.host - SMTP主機 {#section-151df07e7b44446581339bb7abeeba7a}

SMTP電子郵件伺服器的IP地址。

## AS::mailSender.port- SMTP埠 {#section-4b25efca8fd84d5c92dafacd0555e99d}

SMTP電子郵件伺服器的偵聽埠。

## AS::monitorAlertGenerator.messageTo — 郵件收件人 {#section-0017bbaa15434117a70900c3f1163960}

應將警報傳送至的一或多個電子郵件地址。 請使用分號作為分隔符。

## AS::monitorAlertGenerator.messageFrom — 郵件發送者 {#section-db320cba4ac2438ca1cfe6abce4aed87}

應在&#x200B;**[!UICONTROL From]**&#x200B;電子郵件欄位中使用的電子郵件地址。

## AS::monitorAlertGenerator.alertInterval — 監視間隔 {#section-99cb2e3380c1499e9d5aec3671ed73c7}

監視系統將在警報間隔期間累積警報條件，並在每個間隔結束時發送包含所有累積警報的警報電子郵件。 毫秒、整數值、60000或更大。 通常設為5或10分鐘。

## AS::monitorAlertGenerator.heapSpaceResetInterval — 堆空間警報間隔 {#section-fd5a2bf04ed44fdcaef20f77084151a8}

堆空間警報發出後的最短時間。 時間間隔（毫秒） 整數值，0或更大。

## AS::monitorAlertGenerator.minTrafficForAlerts — 啟用警報的最小流量 {#section-8b4db2d6f96642309ca35c49eb3ab230}

每秒請求數。 如果流量低於此臨界值，則不會發出任何回應時間和錯誤警報。 設為0可傳送回應時間和錯誤警報，而不論流量為何。 實際值0或更大。
