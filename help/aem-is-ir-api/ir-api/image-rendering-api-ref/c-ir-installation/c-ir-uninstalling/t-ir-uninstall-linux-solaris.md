---
description: 請依照下列指示，在Linux或Solaris系統上卸載映像渲染。
seo-description: 請依照下列指示，在Linux或Solaris系統上卸載映像渲染。
seo-title: 在Linux和Solaris上卸載
solution: Experience Manager
title: 在Linux和Solaris上卸載
topic: Scene7 Image Serving - Image Rendering API
uuid: 80c0d6ec-985b-4596-bd67-22e5029f7b37
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 在Linux和Solaris上卸載{#uninstalling-on-linux-and-solaris}

請依照下列指示，在Linux或Solaris系統上卸載映像渲染。

在Linux或Solaris系統上卸載映像渲染有兩種方法。

**方法1**

1. 尋找 [!DNL uninstall.sh].

   它位於ImageRendering的安裝源目錄中。 如果此目錄已被刪除，則原始安裝包必須解壓並取消目標以進行解壓 [!DNL uninstall.sh]。
1. 執行 [!DNL uninstall.sh] 並依照畫面上的指示進行。
>**方法2**
>
>1. 使用下列功能停止影像演算： ` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`
>1. 從系統移除ImageRendering。
>
>   
移除ImageRendering的命令取決於您的系統：
>
>   Linux: `rpm -e ImageRendering`
>
>   Solaris: `pkgrm ImageRendering`
>
>1. 刪除步驟2中未刪除的任何目錄或檔案。
>



