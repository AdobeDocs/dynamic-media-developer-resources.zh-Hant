---
description: 必須設定並配置IR 3.x相容性模組。
seo-description: 必須設定並配置IR 3.x相容性模組。
seo-title: 設定和配置IR 3.x相容性模組
solution: Experience Manager
title: 設定和配置IR 3.x相容性模組
topic: Scene7 Image Serving - Image Rendering API
uuid: 609a6ac9-1a4e-4cca-ab08-aa0f957b0e31
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 設定和配置IR 3.x相容性模組{#setup-and-configure-ir-x-compatibility-module}

必須設定並配置IR 3.x相容性模組。

1. Stop `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. 變更為ImageServer網路應用程式目錄。
1. 將目錄的內 [!DNL ir] 容複製到目 [!DNL ROOT] 錄。
1. 在文 [!DNL ROOT/WEB-INF/web.xml] 字編輯器中開啟。
1. 搜尋行 `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. 取消注 `<servlet>` 釋和 `<servlet-mapping>` 標籤。
1. 重新啟動 `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
>**Linux示例**
>
>`cd /usr/local/scene7/ImageServing/webapps/ROOT`
>
>`cp -r ../ir/* ./`
>
>`cd WEB-INF`
>
>然後使用您 [!DNL web.xml]最愛的編輯器進行編輯，以取消注 `<servlet>` 釋和 `<servlet-mapping>` 標籤。
>
>**Windows範例**
>
>開啟Explorer並前往 [!DNL C:\Program Files\Scene7\ImageServing\webapps\ir]。
>
>選擇所有檔案和資料夾，並複製其中的檔案和資料夾 [!DNL C:\Program Files\Scene7\ImageServing\webapps\ROOT]。
>
>然後編輯檔案 [!DNL c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml]，取消注釋 `<servlet>` 和 `<servlet-mapping>` 標籤。

