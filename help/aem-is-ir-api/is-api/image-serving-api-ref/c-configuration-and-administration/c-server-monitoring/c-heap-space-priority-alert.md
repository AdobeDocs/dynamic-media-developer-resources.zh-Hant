---
description: 當空閒Java堆空間在Java垃圾收集週期後立即低於指定的閾值時，將發送優先順序警報。
solution: Experience Manager
title: 堆空間優先順序警報
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: 32951003-386f-4ea2-a5a0-f4d2e6d95ba5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---

# 堆空間優先順序警報{#heap-space-priority-alert}

當空閒Java堆空間在Java垃圾收集週期後立即低於指定的閾值時，將發送優先順序警報。

應通過增加Java堆空間來解決重複的警報。 在以`AS::monitorAlertGenerator.heapSpaceResetInterval`指定的延遲期間過期之前，此條件的後續發生不會導致電子郵件警報。
