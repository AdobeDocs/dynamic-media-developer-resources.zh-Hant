---
description: 使用這些伺服器設定配置警報閾值。
solution: Experience Manager
title: 警報閾值
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: 1ae76692-2688-4902-82a0-d0751408eee7
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---

# 警報閾值{#alert-thresholds}

使用這些伺服器設定配置警報閾值。

## 作為：monitorAlertGenerator.maxAverageResponseTime — 響應時間閾值AS:monitorAlertGenerator.maxAverageResponseTime — 響應時間 {#section-35111039ac6c4a63ba23fc2c828ab726}

當採樣間隔期間處理請求的平均時間超過此處設定的閾值時，將發出響應時間警報。 以毫秒錶示；整數0或更大。 一般值介於100到1000毫秒之間，具體取決於操作的複雜性。

>[!NOTE]
>
>對於此警報，不會考慮導致4xx或5xx回應狀態的請求。

## AS::monitorAlertGenerator.maxErrorRate — 錯誤響應率閾值AS::monitorAlertGenerator.maxErrorRate — 錯誤響應率 {#section-76ba77fd3102419395e0f86719a1f3ec}

當採樣間隔期間HTTP錯誤響應與總響應的比率超過指定閾值時，會發出錯誤警報。

0.0和1.0之間的實際值。通常設定為0.005和0.1之間。設為1可禁用錯誤警報。

## AS::monitorAlertGenerator.minRequestRate — 低流量閾值 {#section-8dfb89ed138640fd86f5ce1dae2a533e}

當當前採樣間隔內每秒接收的平均請求數低於此閾值時，將發送最小流量警報。 將此值設定為0以禁用警報。 以每秒請求數表示。 實際值0或更大。

## AS::monitorAlertGenerator.minFreeHeapSpace -Free Heap Space閾值 {#section-ce6705045f6842769030ccb1894594cc}

指定最小可用Java堆空間。 當可用堆空間低於此閾值時，優先順序警報會在Java垃圾收集週期之後立即發送。 建議50 MB用於平台伺服器的安全操作。 將空閒堆空間保持在此值以上會降低垃圾收集週期的頻率，這可能會提高整體伺服器效能。 以位元組為單位的整數值，0或更大。

## AS::monitorAlertGenerator.maxOverlap — 最大併發請求數 {#section-ddc6925bff944758ab19bcc9cf3f2589}

當平均間隔期間同時處理的請求平均數量超過此臨界值時，會觸發重疊警報。 高重疊可能表示伺服器過載情況。

整數值1或更大。 一般範圍為20到50，視快取點擊率和請求複雜度而定。

## AS::monitorAlertGenerator.lockedThreshold — 鎖定請求閾值 {#section-012a1c9937d445708380339279c62d80}

指定在將請求視為鎖定或掛起之前，該請求必須掛起的秒數。 如果在平均間隔結束時至少有一個請求被擱置超過指定時間段，則發出鎖定的請求警報。 正整數值（毫秒）。

若要處理涉及從外部HTTP伺服器取得資料的複雜轉譯請求和請求，建議將此值設為至少30秒（除非此警報要偵測到此情況）。
