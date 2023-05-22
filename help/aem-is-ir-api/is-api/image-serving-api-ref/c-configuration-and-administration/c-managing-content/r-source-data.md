---
description: Image Serving源資料檔案包括影像和蒙版檔案、字型和ICC配置檔案。
solution: Experience Manager
title: 源資料
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d7e9c101-8d34-4241-b03c-131f31c25933
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---

# 源資料{#source-data}

Image Serving源資料檔案包括影像和蒙版檔案、字型和ICC配置檔案。

映像伺服器必須可訪問所有源資料檔案。 Image Serving提供了許多用於指定資料檔案位置的備選方案：

`*`安裝資料夾`*/ *`根路徑`*/ *`檔案路徑`*`

<table id="simpletable_26686444C7EF46D6BC4C0490C8010BF9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 根路徑</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> IS::RootPath/attribute::RootPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 檔案路徑 </span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalogPath|requestPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 目錄路徑</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 目錄：:Path|catalog::MaskPath|icc::ProfilePath|font::FontPath|font::MetricsPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 請求路徑</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 在Image Serving HTTP請求中指定的相對映像檔案路徑和名稱</span> </p></td> 
 </tr> 
</table>

伺服器從右到左組合路徑段，直到建立絕對檔案路徑。

全部 `*`根路徑`*` 段可以是空的、相對的或絕對的路徑段。

`*`目錄路徑`*` 是絕對或相對檔案路徑/名稱。 `*`請求路徑`*` 必須是相對檔案路徑/名稱。

`Multiple IS::RootPath` 值可以在ImageServerRegistry.xml中定義（或通過管理介面）。 這允許源資料檔案跨多個檔案系統分發。 映像伺服器將按指定的順序嘗試備用路徑，直到找到資料檔案。

可以隨時添加任何類型的新資料檔案，而不停止伺服器。
