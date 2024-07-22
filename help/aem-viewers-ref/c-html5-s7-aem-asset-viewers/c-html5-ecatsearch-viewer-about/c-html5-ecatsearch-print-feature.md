---
description: 檢視器可讓您將目錄內容輸出到印表機。
solution: Experience Manager
title: 列印功能
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: eadcc105-4a86-40f7-867a-3b09a5599a41
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# 列印功能{#print-feature}

檢視器可讓您將目錄內容輸出到印表機。

列印功能是由工具列中的專用按鈕所觸發。 按一下按鈕可讓使用者選擇列印範圍以及每張紙的頁數。

可以使用`printquality`組態引數來調整列印品質。 請注意，不建議將`printquality`設定為大幅高於預設的值。 原因是它會導致使用者端系統上的網頁瀏覽器耗用非常高的記憶體。 此外，請確定為您的Dynamic Media Classic公司設定的影像回應大小上限大於設定的`printquality`值。

>[!NOTE]
>
>除了Internet Explorer 9以外，列印功能僅在桌上型電腦系統上可用。
