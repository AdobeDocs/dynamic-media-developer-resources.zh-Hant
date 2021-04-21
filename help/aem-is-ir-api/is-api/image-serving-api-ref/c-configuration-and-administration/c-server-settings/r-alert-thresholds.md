---
description: 使用這些伺服器設定來配置警報閾值。
solution: Experience Manager
title: 警報閾值
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---


# 警報閾值{#alert-thresholds}

使用這些伺服器設定來配置警報閾值。

## AS:monitorAlertGenerator.maxAverageResponseTime -Response Time ThresholdAS:monitorAlertGenerator.maxAverageResponseTime -Response Time {#section-35111039ac6c4a63ba23fc2c828ab726}

當在採樣間隔期間處理請求的平均時間超過此處設定的閾值時，發出響應時間警報。 以毫秒錶示；整數0或更大。 典型值介於100到1000毫秒之間，具體取決於操作的複雜性。

>[!NOTE]
>
>此警報不會考慮導致4xx或5xx回應狀態的請求。

## AS::monitorAlertGenerator.maxErrorRate —— 錯誤響應速率閾值AS::monitorAlertGenerator.maxErrorRate —— 錯誤響應速率{#section-76ba77fd3102419395e0f86719a1f3ec}

當採樣間隔期間HTTP錯誤響應與總響應的比例超過指定閾值時，發出錯誤警報。

0.0到1.0之間的實際值。通常設定為0.005到0.1之間。設為1可停用錯誤警報。

## AS::monitorAlertGenerator.minRequestRate —— 低流量閾值{#section-8dfb89ed138640fd86f5ce1dae2a533e}

當目前取樣間隔內每秒收到的平均請求數低於此臨界值時，會傳送最小流量警報。 將此值設定為0以禁用警報。 以每秒請求數表示。 實際值0或更大。

## AS::monitorAlertGenerator.minFreeHeapSpace -Free Heap Space閾值{#section-ce6705045f6842769030ccb1894594cc}

指定最小可用Java堆空間。 當可用堆空間低於此閾值時，優先順序警報會在Java廢棄項目收集週期後立即發送。 建議使用50 MB以安全地運行平台伺服器。 將可用堆空間保持在此值以上會降低廢棄項目收集週期的頻率，這可能會改善整體伺服器效能。 整數值（以位元組為單位，0或更大）。

## AS::monitorAlertGenerator.maxOverlap —— 併發請求的最大數量{#section-ddc6925bff944758ab19bcc9cf3f2589}

當平均間隔期間並行處理的平均請求數超過此閾值時，觸發重疊警報。 高重疊可表示可能出現伺服器過載狀況。

整數值1或更大。 一般範圍為20到50，視快取點擊率和要求複雜度而定。

## AS::monitorAlertGenerator.lockedThreshold —— 鎖定的請求閾值{#section-012a1c9937d445708380339279c62d80}

指定請求在被視為鎖定或掛起之前必須等待的秒數。 如果在平均間隔結束時至少一個請求的等待時間超過指定的時間段，則發出鎖定的請求警報。 正整數值（毫秒）。

若要考慮從外部HTTP伺服器取得資料的複雜演算請求和請求，建議將此值設為至少30秒（除非此警報會偵測到此情況）。
