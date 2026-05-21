---
title: 設定IR 3.x相容性模組
description: 設定IR 3.x相容性模組。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 44fbc6be-7681-402a-936a-0511e138365c
TQID: 'https://experienceleague.adobe.com/ce7CdClFrrIFb7fhZRKQ7XBpsNm4BTgwVFHPXy3BXhw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 95
ht-degree: 0%

---

# 設定IR 3.x相容性模組{#setup-and-configure-ir-x-compatibility-module}

1. 停止`<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`。
1. 變更至ImageServer webapps目錄。
1. 將[!DNL ir]目錄的內容複製到[!DNL `ROOT`]目錄。
1. 在文字編輯器中開啟[!DNL `ROOT/WEB-INF/web.xml`]。
1. 搜尋行`<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. 取消註解`<servlet>`和`<servlet-mapping>`標籤。
1. 重新啟動`<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`。

**Linux®範例**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

然後使用您最愛的編輯器編輯[!DNL `web.xml`]以取消註解`<servlet>`和`<servlet-mapping>`標籤。

**Windows範例**

開啟Explorer並移至`C:\Program Files\Scene7\ImageServing\webapps\ir`。

選取所有檔案和資料夾，並複製`C:\Program Files\Scene7\ImageServing\webapps\ROOT`中的檔案和資料夾。

然後編輯檔案`c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml`，取消註解`<servlet>`和`<servlet-mapping>`標籤。
