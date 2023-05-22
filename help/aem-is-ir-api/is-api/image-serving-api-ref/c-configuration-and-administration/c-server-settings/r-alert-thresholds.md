---
description: 使用這些伺服器設定配置警報閾值。
solution: Experience Manager
title: 警報閾值
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 1ae76692-2688-4902-82a0-d0751408eee7
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# 警報閾值{#alert-thresholds}

使用這些伺服器設定配置警報閾值。

## AS:monitorAlertGenerator.maxAverageResponseTime -Response Time ThresholdAS:monitorAlertGenerator.maxAverageResponseTime — 響應時間 {#section-35111039ac6c4a63ba23fc2c828ab726}

當在採樣間隔期間處理請求的平均時間超過此處設定的閾值時，發出響應時間警報。 以毫秒錶示；整數0或更大。 典型值介於100到1000毫秒之間，具體取決於操作的複雜性。

>[!NOTE]
>
>此警報不考慮導致4xx或5xx響應狀態的請求。

## AS::monitorAlertGenerator.maxErrorRate — 錯誤響應速率閾值AS::monitorAlertGenerator.maxErrorRate — 錯誤響應速率 {#section-76ba77fd3102419395e0f86719a1f3ec}

當在採樣間隔期間HTTP錯誤響應與總響應的比率超過指定閾值時，會發出錯誤警報。

0.0到1.0之間的實值。通常設定為0.005到0.1之間。設定為1可禁用錯誤警報。

## AS::monitorAlertGenerator.minRequestRate — 低流量閾值 {#section-8dfb89ed138640fd86f5ce1dae2a533e}

當在當前採樣間隔期間每秒接收的平均請求數低於此閾值時，發送最小通信量警報。 通過將此值設定為0禁用警報。 以每秒請求數表示。 實際值0或更大。

## AS::monitorAlertGenerator.minFreeHeapSpace — 可用堆空間閾值 {#section-ce6705045f6842769030ccb1894594cc}

指定最小可用Java堆空間。 當可用堆空間低於此閾值時，在Java垃圾回收週期後立即發送優先順序警報。 建議50 MB以安全運行 [!DNL Platform Server]。 將空閒堆空間保持在此值以上會減少垃圾回收週期的頻率，這可能會提高整體伺服器效能。 整數值（以位元組為單位）,0或更大。

## AS::monitorAlertGenerator.maxOverlap — 最大併發請求數 {#section-ddc6925bff944758ab19bcc9cf3f2589}

當在平均間隔期間同時處理的平均請求數超過該閾值時觸發重疊警報。 高重疊可表示可能的伺服器過載情況。

整數值1或更大。 典型範圍為20到50，具體取決於快取命中率和請求複雜度。

## AS::monitorAlertGenerator.lockedThreshold — 鎖定請求閾值 {#section-012a1c9937d445708380339279c62d80}

指定請求在被視為鎖定或掛起之前必須掛起的秒數。 如果在平均間隔結束時至少一個請求被掛起的時間超過指定時間段，則發出鎖定的請求警報。 正整數值（毫秒）。

要說明涉及從外部HTTP伺服器獲取資料的複雜呈現請求和請求，建議將此值設定為至少30秒（除非此警報檢測到此情況）。
