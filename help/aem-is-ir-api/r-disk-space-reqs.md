---
title: 磁碟空間需求與建議
description: 除了安裝軟體所需的空間之外，「影像伺服」還有下列磁碟空間需求。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 35486f3f-f0aa-4b69-a1d2-4bc6b5e41c43
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 0%

---

# 磁碟空間需求與建議{#disk-space-requirements-and-recommendations}

除了安裝軟體所需的空間，「影像伺服」的磁碟空間需求如下：

<table id="table_0AE363AB76304F258A19E43500FE8423"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>說明/預設位置/設定方式</b> </th> 
   <th class="entry"> <b>計算/建議</b> </th> 
   <th class="entry"> <b>備註</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>來源影像、字型、ICC設定檔</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/images </span> <span class="codeph"></span> </p> <p> <span class="codeph"> IS：：RootPaths </span> </p> </td> 
   <td> <p>視情況而異；請參閱下方的註解。 </p> </td> 
   <td> <p>只能由影像伺服器存取；伺服器絕不修改資料。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>HTTP回應資料快取</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/cache/is-response </span> </p> <p> <span class="codeph"> PS：：ResponseCacheFolders </span> </p> </td> 
   <td> <p> <span class="codeph"> PlatformServer：：cache.maxSize </span> x 2；建議至少2 GB。 </p> </td> 
   <td> <p>此快取也會儲存巢狀/內嵌資料及外部來源影像。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>影像目錄資料快取</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/cache/catalog </span> </p> <p> <span class="codeph"> CS：：CatalogCacheFolder </span> </p> </td> 
   <td> <p>允許目錄資料夾使用1.5倍的空間。 </p> </td> 
   <td> <p>最初載入目錄時填入。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>記錄資料</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/logs </span> </p> <p> <span class="codeph"> PS：：LogFolder </span> </p> <p> <span class="codeph"> IS：：LogFile </span> </p> <p> <span class="codeph"> SV：：LogFile </span> </p> </td> 
   <td> <p>100 MB或更多。 </p> </td> 
   <td> <p>它依記錄設定和伺服器使用而有所不同。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>影像伺服器暫存檔</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/temp </span> </p> <p> <span class="codeph"> IS：：TempDirectory </span> </p> <p> <span class="codeph"> SV：：TempDirectory </span> </p> </td> 
   <td> <p>100 MB足以應付大部分的使用需求。 </p> </td> 
   <td> <p>短期資料；可能需要PTIFF以外的來源影像和某些回應影像格式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 來源映像的磁碟空間需求 {#section-317da75099ad480d9a461c7e706d4f1c}

Adobe建議您使用「影像轉換器」命令列工具(IC)，將所有來源影像轉換為金字塔TIFF檔案格式(PTIFF)。 此轉換可確保所有應用程式的「影像伺服」執行階段皆獲得最佳效能。 雖然「影像伺服器」可以處理IC接受的所有來源檔案格式，但Dynamic Media不支援這類用途。

使用PTIFF檔案時，下列經驗法則可協助您判斷空間需求。

*`total_space`* （位元組） = *`number_of_images`*  × (2000 + *`avg_pixel_count`* x *`avg_num_components`*  ×  *`p_factor`*)

* *`avg_pixel_count`* 所有原始來源影像的平均畫素大小（寬度x高度）。 例如，如果原始影像通常約為2k×2k畫素，則為4百萬畫素。
* *`avg_num_components`* 視影像型別而定。 若大部分是RGB影像，則為3；若大部分是CMYK或RGBA影像，則為4。 如果一半的影像是RGB，另一半是RGBA，請使用3.5。
* *`p_factor`* 視使用IC轉換影像時的壓縮型別和品質設定而定。

<table id="table_89995BECF30243569954819D07DA2A2F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>PTIFF壓縮</b> </th> 
   <th class="entry"> <b><i>p_factor</i></b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>未壓縮 </p> </td> 
   <td> <p> 33 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Deflate-Compression </p> </td> 
   <td> <p> 25-0.75 （視影像而定） </p> </td> 
  </tr> 
  <tr> 
   <td> <p>JPEG壓縮 </p> </td> 
   <td> <p> 1 (JPEG品質95的典型值) </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此近似值未計入檔案系統額外負荷。 磁碟上的實際空間可能會大很多。

**範例**

「影像伺服」部署預期會使用30,000個低解析度的舊版影像，平均大小為500×500RGB畫素。 新的列印品質影像資料每年新增10,000份。 一般的CMYK影像大小為4k×6k位元組。 所有資料都以高品質進行JPEG壓縮。 使用三年後的磁碟空間總量估計如下：

*`total_space`* = 30,000 × (2k + 0.5k × 0.5k × 3 × 0.1) + 3 × 10,000 × (2k + 4k × 6k × 4 × 0.1) = 2.2 G + 268 GB =約270 GB

為確保最佳品質，可採用zip等壓縮。 假設 *`p_factor`* 當為0.4時，所需的磁碟空間總量大約是四倍大。 在此案例中，會略多於1 TB。
