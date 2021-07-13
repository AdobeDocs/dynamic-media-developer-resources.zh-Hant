---
description: 請按照以下說明卸載Linux或Solaris系統上的映像呈現。
solution: Experience Manager
title: 在Linux和Solaris上卸載
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c81feaba-18da-441a-bfd5-40275558a384
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 1%

---

# 在Linux和Solaris上卸載{#uninstalling-on-linux-and-solaris}

請按照以下說明卸載Linux或Solaris系統上的映像呈現。

在Linux或Solaris系統上卸載Image Rendering有兩種方法。

**方法1**

1. 尋找 [!DNL uninstall.sh].

   它位於安裝ImageRendering的目錄中。 如果此目錄已刪除，則必須解壓縮原始安裝包並取消目標，以提取[!DNL uninstall.sh]。
1. 運行[!DNL uninstall.sh]並按照螢幕上的說明操作。

>**方法2**
>
>1. 停止影像呈現，具有：` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`
>1. 從系統中刪除ImageRendering。

>
>   
刪除ImageRendering的命令取決於您的系統：
>
>   Linux: `rpm -e ImageRendering`
>
>   Solaris:`pkgrm ImageRendering`
>
>1. 刪除步驟2中未刪除的任何目錄或檔案。

>


