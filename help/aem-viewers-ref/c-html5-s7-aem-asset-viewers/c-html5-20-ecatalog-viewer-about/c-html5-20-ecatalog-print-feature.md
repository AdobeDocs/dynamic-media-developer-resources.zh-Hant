---
description: 檢視器可讓您將目錄內容輸出至打印機。
solution: Experience Manager
title: 打印功能
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog
role: Developer,Business Practitioner
exl-id: d7c8a0da-ad8b-440e-b27b-ea85dd975d9d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---

# 打印功能{#print-feature}

檢視器可讓您將目錄內容輸出至打印機。

列印功能由工具列中的專用按鈕觸發。 按一下按鈕可讓使用者選擇列印範圍和每張頁數。

可使用`printquality`配置參數調整打印質量。 請注意，不建議將`printquality`設定為明顯高於預設值的值。 原因在於，客戶端系統上的Web瀏覽器會導致極高的記憶體消耗。 此外，請確定為您的Dynamic Media Classic公司設定的最大影像回應大小大於設定的`printquality`值。

>[!NOTE]
>
>打印功能僅在案頭系統上可用，Internet Explorer 9除外。
