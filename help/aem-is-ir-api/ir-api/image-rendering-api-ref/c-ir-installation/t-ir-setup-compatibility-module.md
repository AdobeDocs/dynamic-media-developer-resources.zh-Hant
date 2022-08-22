---
title: 設定和配置IR 3.x相容模組
description: 設定和配置IR 3.x相容模組。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 44fbc6be-7681-402a-936a-0511e138365c
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 2%

---

# 設定和配置IR 3.x相容模組{#setup-and-configure-ir-x-compatibility-module}

1. Stop `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. 更改到ImageServer Webapps目錄。
1. 複製 [!DNL ir] 目錄 [!DNL `ROOT`] 的子菜單。
1. 開啟 [!DNL `ROOT/WEB-INF/web.xml`] 的子菜單。
1. 搜索行 `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. 取消注釋 `<servlet>` 和 `<servlet-mapping>` 標籤。
1. 重新啟動 `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.

**Linux®示例**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

然後編輯 [!DNL `web.xml`] 使用收藏夾編輯器取消注釋 `<servlet>` 和 `<servlet-mapping>` 標籤。

**Windows示例**

開啟瀏覽器並轉到 `C:\Program Files\Scene7\ImageServing\webapps\ir`。

選擇所有檔案和資料夾並複製其中的檔案和資料夾 `C:\Program Files\Scene7\ImageServing\webapps\ROOT`。

然後編輯檔案 `c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml`，取消注釋 `<servlet>` 和 `<servlet-mapping>` 標籤。
