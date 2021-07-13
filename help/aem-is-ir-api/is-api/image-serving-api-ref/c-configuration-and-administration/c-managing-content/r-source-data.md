---
description: 「影像服務」源資料檔案包括影像和遮色片檔案、字型和ICC配置檔案。
solution: Experience Manager
title: 源資料
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: d7e9c101-8d34-4241-b03c-131f31c25933
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%

---

# 源資料{#source-data}

「影像服務」源資料檔案包括影像和遮色片檔案、字型和ICC配置檔案。

映像伺服器必須可以訪問所有源資料檔案。 「影像伺服」提供許多用於指定資料檔案位置的替代方法：

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
  <td class="stentry"> <p><span class="codeph"> 目錄：:Path|catalog::MaskPath|icc::ProfilePath|font::FontPath|font::MetricsPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> requestPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 在影像伺服HTTP請求中指定的相對影像檔案路徑和名稱</span> </p></td> 
 </tr> 
</table>

伺服器會從右到左組合路徑段，直到建立絕對檔案路徑為止。

所有`*`rootPath`*`區段都可以是空、相對或絕對路徑區段。

`*``*` catalog（目錄）以絕對或相對檔案路徑/名稱分配。`*``*` requestPath必須是相對檔案路徑/名稱。

`Multiple IS::RootPath` 值可在ImageServerRegistry.xml中定義（或透過管理介面定義）。這允許源資料檔案跨多個檔案系統分發。 在找到資料檔案之前，映像伺服器將按指定的順序嘗試替代路徑。

可以隨時添加任何類型的新資料檔案，而無需停止伺服器。
