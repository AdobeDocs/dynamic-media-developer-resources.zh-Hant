---
title: 在Linux®和Solaris™上卸載
description: 按照以下說明在Linux®或Solaris™系統上卸載映像呈現。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c81feaba-18da-441a-bfd5-40275558a384
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 6%

---

# 在Linux®和Solaris™上卸載{#uninstalling-on-linux-and-solaris}

按照以下說明在Linux®或Solaris™系統上卸載映像呈現。 可以使用兩種不同的方法。 進行以下一項操作:

## 方法1

1. 尋找 [!DNL uninstall.sh].

   它位於安裝ImageRendering的目錄中。 如果此目錄已被刪除，則必須解壓縮原始安裝包並取消其標籤才能解壓縮 [!DNL uninstall.sh]。
1. 運行 [!DNL uninstall.sh] 按照螢幕上的說明進行操作。

## 方法2

1. 使用以下方法停止ImageRendering:

   ` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`

1. 從系統中刪除ImageRendering。 您使用的命令取決於您的系統。
   * Linux®: `rpm -e ImageRendering`

   * Solaris™: `pkgrm ImageRendering`

1. 刪除步驟2中未刪除的任何目錄或檔案。

