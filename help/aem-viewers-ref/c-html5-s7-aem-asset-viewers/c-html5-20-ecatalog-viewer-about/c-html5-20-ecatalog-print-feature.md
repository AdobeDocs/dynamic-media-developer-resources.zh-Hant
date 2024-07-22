---
title: 列印功能
description: 檢視器可讓您將目錄內容輸出到印表機。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d7c8a0da-ad8b-440e-b27b-ea85dd975d9d
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---

# 列印功能{#print-feature}

檢視器可讓您將目錄內容輸出到印表機。

列印功能是由工具列中的專用按鈕所觸發。 按一下按鈕可讓使用者選擇列印範圍以及每張紙的頁數。

可以使用`printquality`組態引數來調整列印品質。 不建議將`printquality`設定為高於預設的值。 原因是它會導致使用者端系統上的網頁瀏覽器耗用大量記憶體。 此外，請確定為您的Dynamic Media Classic公司設定的影像回應大小上限大於設定的`printquality`值。

>[!NOTE]
>
>除了Internet Explorer 9以外，列印功能僅在桌上型電腦系統上可用。
