---
description: 必須設定並配置IR 3.x相容性模組。
solution: Experience Manager
title: 設定和配置IR 3.x相容性模組
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 1%

---


# 設定和配置IR 3.x相容模組{#setup-and-configure-ir-x-compatibility-module}

必須設定並配置IR 3.x相容性模組。

1. Stop `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. 變更為ImageServer網路應用程式目錄。
1. 將[!DNL ir]目錄的內容複製到[!DNL ROOT]目錄。
1. 在文字編輯器中開啟[!DNL ROOT/WEB-INF/web.xml]。
1. 搜索行`<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. 取消對`<servlet>`和`<servlet-mapping>`標籤的注釋。
1. 重新啟動 `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.

**Linux示例**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

然後使用您最愛的編輯器編輯[!DNL web.xml]，以取消對`<servlet>`和`<servlet-mapping>`標籤的註解。

**Windows範例**

開啟Explorer並轉至`C:\Program Files\Scene7\ImageServing\webapps\ir`。

選擇所有檔案和資料夾，並複製`C:\Program Files\Scene7\ImageServing\webapps\ROOT`內部的檔案和資料夾。

然後編輯檔案`c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml`，取消對`<servlet>`和`<servlet-mapping>`標籤的註解。
