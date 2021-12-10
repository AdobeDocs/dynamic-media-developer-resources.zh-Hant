---
title: 打印功能
description: 檢視器可讓您將目錄內容輸出至打印機。
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

檢視器可讓您將目錄內容輸出至打印機。

列印功能由工具列中的專用按鈕觸發。 按一下按鈕可讓使用者選擇列印範圍和每張頁數。

可使用 `printquality` 設定參數。 設定 `printquality` 不建議設定為高於預設值的值。 原因是客戶端系統上的Web瀏覽器會導致記憶體消耗高。 此外，請確定為您的Dynamic Media Classic公司設定的最大影像回應大小大於設定的 `printquality` 值。

>[!NOTE]
>
>打印功能僅在案頭系統上可用，Internet Explorer 9除外。
