---
description: 必須設定和配置IR 3.x相容性模組。
solution: Experience Manager
title: 設定和配置IR 3.x相容模組
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 44fbc6be-7681-402a-936a-0511e138365c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 1%

---

# 設定和配置IR 3.x相容模組{#setup-and-configure-ir-x-compatibility-module}

必須設定和配置IR 3.x相容性模組。

1. Stop `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. 更改到ImageServer Webapps目錄。
1. 將[!DNL ir]目錄的內容複製到[!DNL ROOT]目錄。
1. 在文字編輯器中開啟[!DNL ROOT/WEB-INF/web.xml]。
1. 搜尋行`<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. 取消對`<servlet>`和`<servlet-mapping>`標籤的註解。
1. 重新啟動 `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.

**Linux範例**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

然後，使用您最喜愛的編輯器編輯[!DNL web.xml]以取消對`<servlet>`和`<servlet-mapping>`標籤的註解。

**Windows範例**

開啟Explorer並轉至`C:\Program Files\Scene7\ImageServing\webapps\ir`。

選擇所有檔案和資料夾，並複製`C:\Program Files\Scene7\ImageServing\webapps\ROOT`內的檔案和資料夾。

然後編輯檔案`c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml`，取消對`<servlet>`和`<servlet-mapping>`標籤的註解。
