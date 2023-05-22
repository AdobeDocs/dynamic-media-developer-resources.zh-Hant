---
description: 查看器允許您將目錄內容輸出到打印機。
solution: Experience Manager
title: 打印功能
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: eadcc105-4a86-40f7-867a-3b09a5599a41
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 0%

---

# 打印功能{#print-feature}

查看器允許您將目錄內容輸出到打印機。

打印功能由工具欄中的專用按鈕觸發。 按一下該按鈕，用戶可以選擇打印範圍和每張紙的頁數。

打印的質量可以使用 `printquality` 配置參數。 注意設定 `printquality` 不建議將值設定為顯著高於預設值。 原因是客戶端系統上的Web瀏覽器會導致很高的記憶體消耗。 另外，確保為您的Dynamic Media Classic公司設定的最大映像響應大小大於配置的 `printquality` 值。

>[!NOTE]
>
>「打印」功能僅在案頭系統上可用，Internet Explorer 9除外。
