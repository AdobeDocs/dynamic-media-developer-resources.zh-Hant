---
title: 在Linux®和Solaris™上解除安裝
description: 請依照下列指示，在Linux®或Solaris™系統上解除安裝「影像演算」。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c81feaba-18da-441a-bfd5-40275558a384
TQID: 'https://experienceleague.adobe.com/RmD5z5300Nw12kSsOretyAl5p-TeFkox-Cyqm1MrF5w'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 120
ht-degree: 4%

---

# 在Linux®和Solaris™上解除安裝{#uninstalling-on-linux-and-solaris}

請依照下列指示，在Linux®或Solaris™系統上解除安裝「影像演算」。 有兩種不同的方法可供您使用。 進行以下一項操作:

## 方法1

1. 尋找[!DNL uninstall.sh]。

   它位於ImageRendering的安裝目錄中。 如果已經移除此目錄，則必須解壓縮原始安裝封裝，並取消啟動以解壓縮[!DNL uninstall.sh]。
1. 執行[!DNL uninstall.sh]並遵循熒幕上的指示。

## 方法2

1. 使用下列專案停止ImageRendering：

   ` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`

1. 從您的系統中移除ImageRendering。 您使用的指令取決於您的系統。
   * Linux®： `rpm -e ImageRendering`

   * Solaris™： `pkgrm ImageRendering`

1. 刪除步驟2中未移除的任何目錄或檔案。


