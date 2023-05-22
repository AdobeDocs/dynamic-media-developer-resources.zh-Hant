---
description: 當空閒Java堆空間在緊隨Java垃圾回收循環後低於指定閾值時，將發送優先順序警報。
solution: Experience Manager
title: 堆空間優先順序警報
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 32951003-386f-4ea2-a5a0-f4d2e6d95ba5
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 0%

---

# 堆空間優先順序警報{#heap-space-priority-alert}

當空閒Java堆空間在緊隨Java垃圾回收循環後低於指定閾值時，將發送優先順序警報。

應通過增加Java堆空間來解決重複的警報。 此條件的後續出現在指定的延遲期間之前不會生成電子郵件警報 `AS::monitorAlertGenerator.heapSpaceResetInterval` 已過期。
