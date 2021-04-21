---
description: 「影像伺服」來源資料檔案包括影像和遮色片檔案、字型和ICC描述檔。
solution: Experience Manager
title: 來源資料
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---


# 源資料{#source-data}

「影像伺服」來源資料檔案包括影像和遮色片檔案、字型和ICC描述檔。

映像伺服器必須可以訪問所有源資料檔案。 「影像伺服」提供多種替代方式，以指定資料檔案的位置：

`*`install_`*/ *``*/ *`folderrootPathfilePath`*`

<table id="simpletable_26686444C7EF46D6BC4C0490C8010BF9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rootPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> IS::RootPath/attribute::RootPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> filePath  </span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalogPath|requestPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> catalogPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalog::Path|catalog::MaskPath|icc::ProfilePath|font::FontPath|font::MetricsPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> requestPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 影像伺服HTTP請求中指定的相對影像檔案路徑和名稱</span> </p></td> 
 </tr> 
</table>

伺服器會從右至左組合路徑區段，直到建立絕對檔案路徑為止。

所有`*`rootPath`*`區段都可以是空的、相對的或絕對的路徑區段。

`*`目`*` 錄以絕對或相對檔案路徑／名稱填入。`*``*` requestPath必須是相對檔案路徑／名稱。

`Multiple IS::RootPath` 值可在ImageServerRegistry.xml中定義（或透過管理介面）。這允許源資料檔案跨多個檔案系統分發。 影像伺服器會依指定順序嘗試替代路徑，直到找到資料檔案為止。

不需停止伺服器，就可隨時新增任何類型的資料檔案。
