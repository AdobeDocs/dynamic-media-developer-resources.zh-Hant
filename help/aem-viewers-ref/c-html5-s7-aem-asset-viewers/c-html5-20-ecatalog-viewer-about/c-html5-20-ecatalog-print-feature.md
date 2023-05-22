---
title: 打印功能
description: 查看器允許您將目錄內容輸出到打印機。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d7c8a0da-ad8b-440e-b27b-ea85dd975d9d
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---

# 打印功能{#print-feature}

查看器允許您將目錄內容輸出到打印機。

打印功能由工具欄中的專用按鈕觸發。 按一下該按鈕，用戶可以選擇打印範圍和每張紙的頁數。

打印的質量可以使用 `printquality` 配置參數。 設定 `printquality` 不建議將值設定為高於預設值。 原因是客戶端系統上的Web瀏覽器會導致高記憶體消耗。 另外，確保為您的Dynamic Media Classic公司設定的最大映像響應大小大於配置的 `printquality` 值。

>[!NOTE]
>
>「打印」功能僅在案頭系統上可用，Internet Explorer 9除外。
