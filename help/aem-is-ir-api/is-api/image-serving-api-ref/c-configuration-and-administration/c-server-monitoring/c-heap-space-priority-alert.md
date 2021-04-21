---
description: 當空閒Java堆空間在緊接Java廢棄項目收集週期後的指定閾值以下時，會發送優先順序警報。
solution: Experience Manager
title: 堆空間優先順序警報
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---


# 堆空間優先順序警報{#heap-space-priority-alert}

當空閒Java堆空間在緊接Java廢棄項目收集週期後的指定閾值以下時，會發送優先順序警報。

應通過增加Java堆空間來解決重複警報。 在以`AS::monitorAlertGenerator.heapSpaceResetInterval`指定的延遲期間過期之前，此條件的後續發生不會導致電子郵件警報。
