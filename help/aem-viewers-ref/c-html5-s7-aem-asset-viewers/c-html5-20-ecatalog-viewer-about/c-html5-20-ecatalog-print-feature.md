---
description: 檢視器可讓您將目錄內容輸出至印表機。
seo-description: 檢視器可讓您將目錄內容輸出至印表機。
seo-title: 列印功能
solution: Experience Manager
title: 列印功能
uuid: 4ff170a3-ce37-454f-b4b0-b323de3dc9c9
feature: Dynamic Media經典，檢視器，SDK/API,eCatalog
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 0%

---


# 列印功能{#print-feature}

檢視器可讓您將目錄內容輸出至印表機。

列印功能是由工具列中的專用按鈕觸發。 按一下按鈕可讓使用者選擇列印範圍和每張頁面的數目。

使用`printquality`配置參數可調整打印質量。 請注意，不建議將`printquality`設定為明顯高於預設值的值。 原因是客戶端系統上的Web瀏覽器會佔用很多記憶體。 此外，請確定您的Dynamic MediaClassic公司設定的影像回應大小上限大於設定的`printquality`值。

>[!NOTE]
>
>「列印」功能僅適用於案頭系統，Internet Explorer 9除外。

